<template>
  <div class="ios w-full min-h-screen flex flex-col text-center text-gray-700 dark:text-gray-200">
    <div class="flex-auto">
      <router-view />
    </div>
    <Footer />
  </div>
</template>

<style>
.ios {
  padding-bottom: calc(50px + env(safe-area-inset-bottom));
}
</style>
