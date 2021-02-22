<template>
  <div class="nav-menu-item">
    <!-- <app-button></app-button> -->
    <slot></slot>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.nav-menu-item {
  padding: 0.75rem;
  margin-right: 2.25rem;
  font-size: 1.065rem;
  text-transform: capitalize;
  color: rgb(255 255 255 / 50%);
  cursor: pointer;
  text-transform: uppercase;
}

.nav-menu-item:hover {
  color: rgb(255 255 255 / 75%);
}

.nav-menu-item:last-child {
  margin-right: 0;
}
</style>
