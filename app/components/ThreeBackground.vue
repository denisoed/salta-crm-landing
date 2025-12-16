<template>
  <div ref="containerEl" class="fixed inset-0 -z-10" :style="containerStyle" />
</template>

<script setup lang="ts">
import { onBeforeUnmount, onMounted, ref } from 'vue'

declare global {
  interface Window {
    THREE?: any
    __threeCdnPromise?: Promise<void>
  }
}

const containerEl = ref<HTMLDivElement | null>(null)

const containerStyle = {
  background: 'linear-gradient(180deg, #ffffff 0%, #f8fafc 100%)',
} as const

function loadThreeFromCdn() {
  if (window.THREE) return Promise.resolve()
  if (window.__threeCdnPromise) return window.__threeCdnPromise

  window.__threeCdnPromise = new Promise<void>((resolve, reject) => {
    const script = document.createElement('script')
    script.src = 'https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js'
    script.async = true
    script.onload = () => resolve()
    script.onerror = () => reject(new Error('Failed to load three.js from CDN'))
    document.head.appendChild(script)
  })

  return window.__threeCdnPromise
}

let rafId: number | null = null
let cleanupFns: Array<() => void> = []

onMounted(async () => {
  const container = containerEl.value
  if (!container) return

  await loadThreeFromCdn()
  const THREE = window.THREE
  if (!THREE) return

  const scene = new THREE.Scene()
  scene.background = new THREE.Color(0xffffff)
  scene.fog = new THREE.Fog(0xffffff, 10, 50)

  const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000)
  camera.position.z = 30
  camera.position.y = 10
  camera.lookAt(0, 0, 0)

  const renderer = new THREE.WebGLRenderer({ alpha: true, antialias: true })
  renderer.setSize(window.innerWidth, window.innerHeight)
  renderer.setPixelRatio(window.devicePixelRatio)
  container.appendChild(renderer.domElement)

  // Particles wave geometry (50 x 40)
  const particlesGeometry = new THREE.BufferGeometry()
  const separation = 3
  const amountX = 50
  const amountY = 40
  const count = amountX * amountY

  const positions = new Float32Array(count * 3)
  const scales = new Float32Array(count)

  let i = 0
  let j = 0
  for (let ix = 0; ix < amountX; ix++) {
    for (let iy = 0; iy < amountY; iy++) {
      positions[i] = ix * separation - (amountX * separation) / 2
      positions[i + 1] = 0
      positions[i + 2] = iy * separation - (amountY * separation) / 2
      scales[j] = 1
      i += 3
      j++
    }
  }

  particlesGeometry.setAttribute('position', new THREE.BufferAttribute(positions, 3))
  particlesGeometry.setAttribute('scale', new THREE.BufferAttribute(scales, 1))

  const material = new THREE.PointsMaterial({
    color: 0x3b82f6,
    size: 0.4,
    transparent: true,
    opacity: 0.6,
  })

  const particles = new THREE.Points(particlesGeometry, material)
  scene.add(particles)

  let step = 0
  let mouseX = 0
  let mouseY = 0

  const onResize = () => {
    camera.aspect = window.innerWidth / window.innerHeight
    camera.updateProjectionMatrix()
    renderer.setSize(window.innerWidth, window.innerHeight)
  }

  const onMouseMove = (e: MouseEvent) => {
    mouseX = (e.clientX / window.innerWidth) * 2 - 1
    mouseY = -(e.clientY / window.innerHeight) * 2 + 1
  }

  window.addEventListener('resize', onResize, { passive: true })
  window.addEventListener('mousemove', onMouseMove, { passive: true })
  cleanupFns.push(() => window.removeEventListener('resize', onResize))
  cleanupFns.push(() => window.removeEventListener('mousemove', onMouseMove))

  const animate = () => {
    rafId = requestAnimationFrame(animate)

    const arr = particles.geometry.attributes.position.array as Float32Array
    let k = 0
    for (let ix = 0; ix < amountX; ix++) {
      for (let iy = 0; iy < amountY; iy++) {
        arr[k + 1] = Math.sin((ix + step) * 0.3) * 2 + Math.sin((iy + step) * 0.5) * 2
        k += 3
      }
    }

    particles.geometry.attributes.position.needsUpdate = true
    particles.rotation.y += 0.001
    step += 0.05

    camera.position.x += (mouseX * 10 - camera.position.x) * 0.02
    camera.position.y += (10 + mouseY * 5 - camera.position.y) * 0.02
    camera.lookAt(scene.position)

    renderer.render(scene, camera)
  }

  animate()

  cleanupFns.push(() => {
    if (rafId) cancelAnimationFrame(rafId)
    rafId = null
  })

  cleanupFns.push(() => {
    scene.remove(particles)
    particlesGeometry.dispose()
    material.dispose()
    renderer.dispose()
    if (renderer.domElement && renderer.domElement.parentNode) {
      renderer.domElement.parentNode.removeChild(renderer.domElement)
    }
  })
})

onBeforeUnmount(() => {
  for (const fn of cleanupFns.splice(0)) fn()
})
</script>


