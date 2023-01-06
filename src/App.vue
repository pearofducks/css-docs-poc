<script setup>
import Box from './components/Box.vue'
import Container from './components/Container.vue'
</script>

<template>
  <container>
    <box striped class="flex gap-4">
      <div class="w-32 p-4 rounded-2 bg-blue-500 text-white flex items-center justify-center">
        01
      </div>
      <div class="w-64 p-4 rounded-2 bg-blue-500 text-white flex items-center justify-center">
        02
      </div>
      <div class="w-64 p-4 rounded-2 bg-blue-500 text-white flex items-center justify-center">
        03
      </div>
    </box>
  </container>
</template>
