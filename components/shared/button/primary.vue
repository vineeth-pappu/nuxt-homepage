<template>
  <app-button class="primary-btn" :text-uppercase="textUppercase">
    <slot></slot>
  </app-button>
</template>

<script>
export default {
  props: {
    textUppercase: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style scoped>
.primary-btn {
  background: linear-gradient(90deg, #e50612, #730309);
}
.primary-btn::before {
  background: linear-gradient(90deg, #730309, #e50612);
}
</style>
