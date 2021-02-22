<template>
  <header>
    <app-logo-monochrome></app-logo-monochrome>
    <app-header-nav-menu></app-header-nav-menu>
  </header>
</template>

<script>
export default {}
</script>

<style scoped>
header {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 105px;
  border-bottom: 1px solid rgb(255 255 255 / 50%);
  padding: 1rem 7rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: transparent;
  z-index: 10;
}
</style>
