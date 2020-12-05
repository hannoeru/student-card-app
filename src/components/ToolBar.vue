<template>
  <div v-if="show" class="toolbar fixed top-0 w-full bg-white dark:bg-gray-850 border-b py-3 text-xl font-medium tracking-wide z-50 shadow-sm">
    <h1>{{ title }}</h1>
  </div>
  <div class="toolbar w-full mt-12 mb-2 flex px-5">
    <div class="flex-auto text-left text-4xl font-bold">
      <h1>{{ title }}</h1>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref, defineProps } from 'vue'

const props = defineProps({
  title: String,
})

window.onscroll = function() { scrollFunction() }

const show = ref(false)

const scrollFunction = () => {
  if (document.body.scrollTop > 10 || document.documentElement.scrollTop > 20)
    show.value = true
  else
    show.value = false
}
</script>

<style>
.toolbar {
  padding-top: env(safe-area-inset-top);
}
</style>
