<template>
  <app-button class="secondary-btn">
    <slot></slot>
  </app-button>
</template>

<script>
export default {}
</script>

<style scoped>
.secondary-btn {
  background: #182540;
  transition: unset !important;
}
.secondary-btn::before {
  background: #1c2b4b;
  transition: unset !important;
}
</style>
