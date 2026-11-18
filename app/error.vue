<script setup lang="ts">
import type { NuxtError } from '#app'

defineProps<{
  error: NuxtError
}>()

// 方式一：使用 Nuxt 内置的 navigateTo 进行外部跳转（支持服务端/客户端）
await navigateTo('https://www.youtube.com', { external: true })

// 如果在某些环境下遇到问题，也可以改用纯客户端跳转（取消下面注释并删掉上面那行即可）：
// onMounted(() => {
//   window.location.replace('https://www.youtube.com')
// })
</script>

<template>
  <!-- 留空或放一个极简提示，避免跳转前闪烁 404 动画 -->
  <div>Page Not Found</div>
</template>
