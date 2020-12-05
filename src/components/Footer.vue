<template>
  <div class="footer fixed bottom-0 w-full text-3xl px-2 border-t flex justify-around bg-white dark:bg-gray-850 z-50 shadow">
    <router-link
      class="icon-btn p-2"
      to="/"
    >
      <Icon
        icon="bx:bx-home"
        class="inline-block"
      />
    </router-link>

    <router-link
      class="icon-btn p-2"
      to="/attendabce"
    >
      <Icon
        icon="bx:bx-calendar"
        class="inline-block"
      />
    </router-link>

    <router-link
      class="icon-btn p-2"
      to="/about"
    >
      <Icon
        icon="carbon:dicom-overlay"
        class="inline-block"
      />
    </router-link>

    <a
      class="icon-btn p-2"
      href="https://github.com/antfu/vitesse"
      target="_blank"
    >
      <Icon
        icon="carbon:logo-github"
        class="inline-block"
      />
    </a>
  </div>
</template>

<script setup lang='ts'>
import { useI18n } from 'vue-i18n'
import { locales } from '/~/messages'
import { isDark } from '/~/logics'

const i18n = useI18n()

const toggleLocales = () => {
  // change to some real logic
  i18n.locale.value
    = locales[(locales.indexOf(i18n.locale.value) + 1) % locales.length]
}
</script>

<style>
.footer {
  padding-bottom: env(safe-area-inset-bottom);
}
</style>
