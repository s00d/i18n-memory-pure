<template>
  <span>{{ timeLabel }}</span>
</template>

<script lang="ts" setup>
defineI18nRoute({
  locales: ['en']
})

const { $i18n } = useNuxtApp()

await new Promise(resolve => setTimeout(resolve, 10))

const timeLabel = computed(() => $i18n.t('general'))
</script>

