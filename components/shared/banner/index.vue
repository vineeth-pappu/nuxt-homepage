<template>
  <div class="banner">
    <img
      src="https://admin.m2-wunschauto.at/wp-content/uploads/2021/02/herobg.jpg"
      alt="banner"
    />
    <div class="banner-overlay"></div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>
.banner {
  position: absolute;
  width: 100%;
  height: 100%;
  z-index: -1;
}
.banner img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.banner-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.3);
}
</style>
