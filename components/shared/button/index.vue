<template>
  <button class="btn app-btn">
    <slot></slot>
  </button>
</template>

<script>
export default {}
</script>

<style scoped>
.app-btn {
  position: relative;
  /* background: linear-gradient(90deg, #e50612, #730309); */
  font-size: 1.125rem;
  color: #fff;
  outline: none;
  border: none;
  box-shadow: none;
  border-radius: 50px;
  padding: 1.25rem 3.75rem;
  text-transform: capitalize;
  transition: all 0.5s linear;
  overflow: hidden;
  z-index: 1;
}
.app-btn::before {
  position: absolute;
  content: '';
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  /* background: linear-gradient(90deg, #730309, #e50612); */
  z-index: -1;
  opacity: 0;
  transition: all 0.5s linear;
}
.app-btn:hover::before {
  opacity: 1;
}
</style>
