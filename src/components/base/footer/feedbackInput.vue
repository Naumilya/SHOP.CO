<template>
  <input type="text" placeholder="Enter your email address" :class="$style.feedbackInput" />
</template>

<script setup lang="ts"></script>

<style module lang="scss">
@use '@/scss/variables.scss';
.feedbackInput {
  padding: 12px 0 14px 52px;
  background: variables.$white;
  border: none;
  outline: none;
  border-radius: 62px;
  background-image: url('@/assets/svgs/mail.svg');
  background-repeat: no-repeat;
  background-position: 16px center;
}
</style>
