<template>
  <div class="w-full px-4 text-left py-2">
    <div class="my-2 font-semibold text-xs opacity-70">
      <h2>{{ title }}</h2>
    </div>
    <ul>
      <li>
        <ListItem v-for="item in items" :key="item.title" :item="item" />
      </li>
    </ul>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  items: Array,
  title: {
    type: String,
    default: 'お知らせ',
  },
})
</script>

<style>

</style>
