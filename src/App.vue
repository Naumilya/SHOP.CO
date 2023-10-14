<template>
  <TheHeader />
  <RouterView />
  <TheFooter />
</template>

<script setup lang="ts">
import TheFooter from '@/components/base/footer/TheFooter.vue'
import TheHeader from '@/components/base/header/TheHeader.vue'

import { RouterView } from 'vue-router'
</script>

<style scoped></style>
