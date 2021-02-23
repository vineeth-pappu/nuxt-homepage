<template>
  <section class="home-banner">
    <app-banner :image="data.background_image"></app-banner>
    <div class="banner-logo">
      <app-logo-monochrome></app-logo-monochrome>
    </div>
    <h1 class="banner-title">
      {{ data.title }}
    </h1>
    <h4 class="banner-caption">
      {{ data.subtitle }}
    </h4>
    <div class="banner-cta">
      <app-button-primary :text-uppercase="true">
        {{ data.button_1 }}
      </app-button-primary>
      <app-button-secondary :text-uppercase="true">
        {{ data.button_2 }}
      </app-button-secondary>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      default() {
        return {}
      },
    },
  },

  data() {
    return {}
  },

  mounted() {
    console.log('banner', this.data)
  },
}
</script>

<style scoped>
.home-banner {
  position: relative;
  width: 100%;
  height: 100vh;
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
