<script setup>
import Box from './components/Box.vue'
import Container from './components/Container.vue'
import WidthController from './components/WidthController.vue'
</script>

<template>
  <width-controller>
  <container>
    <box striped class="flex gap-4" fg-color="rgba(2,132,199, 0.5)">
      <div class="w-32 p-4 rounded-2 bg-sky-300 text-white flex items-center justify-center">
        01
      </div>
      <div class="w-64 p-4 rounded-2 bg-sky-600 text-white flex items-center justify-center">
        02
      </div>
      <div class="w-64 p-4 rounded-2 bg-sky-600 text-white flex items-center justify-center">
        03
      </div>
    </box>
  </container>
</width-controller>
</template>
