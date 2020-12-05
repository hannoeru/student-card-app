<template>
  <div class="py-2">
    <h3 class="font-semibold">
      {{ item.title }}
    </h3>
    <p class="opacity-70 font-light">
      {{ item.content }}
    </p>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  item: Object,
})

</script>

<style>

</style>
