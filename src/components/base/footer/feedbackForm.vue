<template>
  <form :class="$style.feadbackForm">
    <div :class="$style.feadbackFormInner">
      <h2 :class="$style.feadbackFormTitle">
        <slot name="title"></slot>
      </h2>
      <div :class="$style.feadbackFormAction">
        <feedbackInput />
        <BaseButton :class="$style.button_white" :path="'#'" @click.prevent
          >Subscribe to Newsletter</BaseButton
        >
      </div>
    </div>
  </form>
</template>

<script setup lang="ts">
import BaseButton from '@/components/base/button/BaseButton.vue'
import feedbackInput from '@/components/base/footer/feedbackInput.vue'
</script>

<style module lang="scss">
@use '@/scss/fonts.scss';
@use '@/scss/variables.scss';

.feadbackForm {
  margin-top: 80px;
  background-color: variables.$black;
  padding: 32px 64px;
  border-radius: 20px;
  .feadbackFormInner {
    display: flex;
    align-items: center;
    justify-content: space-between;

    .feadbackFormTitle {
      @include fonts.text-headline-h3;
      max-width: 551px;
      color: variables.$white;
    }

    .feadbackFormAction {
      display: flex;
      flex-direction: column;
      row-gap: 14px;

      .button_white {
        background: variables.$white;
        color: variables.$black;

        &:hover {
          border: 1px solid variables.$black;
          transition: border 0.5s ease-in-out;
        }
      }
    }
  }
}
</style>
