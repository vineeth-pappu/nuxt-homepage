<template>
  <app-button class="primary-btn">
    <slot></slot>
  </app-button>
</template>

<script>
export default {}
</script>

<style scoped>
.primary-btn {
  background: linear-gradient(90deg, #e50612, #730309);
}
.primary-btn::before {
  background: linear-gradient(90deg, #730309, #e50612);
}
</style>
