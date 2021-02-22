<template>
  <section class="home-banner">
    <app-banner></app-banner>
    <div class="banner-logo">
      <app-logo-monochrome></app-logo-monochrome>
    </div>
    <h1 class="banner-title">Find the car you want</h1>
    <h4 class="banner-caption">
      M2 is your platform for a smooth car buying and selling.
    </h4>
    <div class="banner-cta">
      <app-button-primary>M2 FINDES</app-button-primary>
      <app-button-secondary>M2 advertised</app-button-secondary>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style scoped>
.home-banner {
  position: relative;
  width: 100%;
  height: 124vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.banner-logo {
  height: 72px;
  margin: 1.75rem auto;
}
h1.banner-title {
  font-style: italic;
  color: #fff;
}
h4.banner-caption {
  font-size: 1.0625rem;
  color: #fff;
}
.banner-cta {
  display: flex;
  margin: 2rem auto;
}
.banner-cta button {
  margin: 0 1rem;
}
</style>
