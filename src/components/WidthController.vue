<script setup>
import { provide, watch, ref } from 'vue'
import { useDraggable } from '@vueuse/core'

const right = ref(0)
const wrapperEl = ref(null)
const containerEl = ref(null)
const handleEl = ref(null)
provide('widthController', { register: (c) => containerEl.value = c })

const { x } = useDraggable(handleEl)
watch(x, () => {
  const wrapperRight = wrapperEl.value.getBoundingClientRect().right
  right.value = wrapperRight - x.value
  if (right.value < 0) right.value = 0
})

watch(right, () => {
  containerEl.value.style.marginRight = right.value + 'px'
  handleEl.value.style.transform = `translateX(-${right.value}px)`
})
</script>

<template>
  <div class="relative pr-8" ref="wrapperEl">
    <slot />
    <div ref="handleEl" @mousedown="handleDragStart" @touchstart="handleDragStart" class="absolute rounded-full right-0 top-0 bottom-0 flex items-center cursor-ew-resize">
      <div class="h-16 w-4 rounded-full bg-gray-600" />
    </div>
  </div>
</template>
