<template>
  <div class="relative">
    <ToolBar :title="title" />
    <div class="p-5 space-y-4">
      <slot />
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  title: String,
})
</script>
