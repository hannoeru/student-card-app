<template>
  <Container title="ホーム">
    <StudentCard :student-info="studentInfo" />
    <NotificationList :items="notifications" />
  </Container>
</template>

<script setup lang='ts'>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
import { useI18n } from 'vue-i18n'

const name = ref('')

const router = useRouter()
const go = () => {
  if (name.value) router.push(`/hi/${name.value}`)
}

const { t } = useI18n()
const studentInfo = ref({
  id: '20C1010000',
  name: 'TECH.C.',
  subject: 'スーパーIT科',
  birthday: 'YYYY/MM/DD',
})

interface Notification {
  title: string
  content: string
}

const notifications = ref<Notification[]>([
  {
    title: 'Matched Geometry Effect',
    content: 'Learn how to quickly transition different views',
  },
  {
    title: 'Design a Widget in Figma',
    content: 'Learn how to design an App Widget of different sizes.',
  },
  {
    title: 'Design for App Clip',
    content: 'Learn how to design an App Widget of different sizes.',
  },
  {
    title: 'Create a Widget in SwiftUI',
    content: 'Build your own App Widget for your app using WidgetKit',
  },
  {
    title: 'Create a Widget in SwiftUI',
    content: 'Build your own App Widget for your app using WidgetKit',
  },
  {
    title: 'Create a Widget in SwiftUI',
    content: 'Build your own App Widget for your app using WidgetKit',
  },
  {
    title: 'Create a Widget in SwiftUI',
    content: 'Build your own App Widget for your app using WidgetKit',
  },
  {
    title: 'Create a Widget in SwiftUI',
    content: 'Build your own App Widget for your app using WidgetKit',
  },
])
</script>
