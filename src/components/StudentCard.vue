<template>
  <div class="relative w-full border rounded-3xl p-4 grid gap-3 grid-cols-7 text-sm shadow-md">
    <div class="col-span-4 text-left font-semibold">
      東京デザインテクノロジーセンター専門学校
    </div>
    <div class="col-span-3 flex justify-end items-center">
      <h2 class="font-bold">
        Student ID
      </h2>
      <img
        src="/~/assets/logo.png"
        alt="Logo"
        class="h-10 ml-3"
      >
    </div>
    <div class="col-span-3 flex justify-center">
      <img
        src="/~/assets/user-image.png"
        alt="Logo"
        class="h-20 rounded-xl"
      >
    </div>
    <div class="col-span-4 flex items-center text-xs">
      <div class="flex-auto opacity-70 text-right">
        <ul>
          <li>学籍番号：</li>
          <li>氏名：</li>
          <li>学科：</li>
          <li>生年月日：</li>
        </ul>
      </div>
      <div class="flex-auto font-semibold text-left ml-2">
        <ul>
          <li v-for="item in studentInfo" :key="item">
            {{ item }}
          </li>
        </ul>
      </div>
    </div>
    <div class="col-span-4 text-left text-xs">
      <p>〒169-0075 東京都新宿区高田馬場2-11-10</p>
      <p>TEL 03-3209-8222</p>
    </div>
    <div class="col-span-3 text-right text-xs">
      <p>上記の者は当校の学生であることを証明する</p>
      <p><span class="font-semibold mr-2">学園長</span>多田順次</p>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps({
  studentInfo: Object,
  image: String,
})
</script>

<style>

</style>
