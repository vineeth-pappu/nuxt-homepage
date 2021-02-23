<template>
  <div class="banner">
    <img :src="image.url" alt="banner" />
    <div class="banner-overlay" :style="{ background: tint }"></div>
  </div>
</template>

<script>
export default {
  props: {
    image: {
      type: Object,
      default() {
        return { url: '' }
      },
    },
    tint: {
      type: String,
      default: 'rgba(0, 0, 0, 0.3)',
    },
  },
}
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
}
</style>
