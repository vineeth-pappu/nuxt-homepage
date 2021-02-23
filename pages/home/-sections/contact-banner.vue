<template>
  <section class="contact-banner">
    <app-banner
      :image="data.background_image"
      tint="rgba(0, 0, 0, 0.4)"
    ></app-banner>
    <div class="container">
      <h2 class="contact-title">{{ data.title }}</h2>
      <h5 class="contact-description">{{ data.description }}</h5>
      <app-button-primary :text-uppercase="true">
        {{ data.button }}
      </app-button-primary>
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
}
</script>

<style scoped>
.contact-banner {
  height: 95vh;
  position: relative;
  display: flex;
  align-items: center;
}
.contact-title {
  font-family: 'Lora', serif;
  font-size: 2.625rem;
  font-weight: 500;
  color: #fff;
  padding-bottom: 1rem;
  margin-bottom: 0;
}
.contact-description {
  color: #fff;
  width: 80%;
  padding-bottom: 1rem;
  font-size: 1.0625rem;
  line-height: 1.5;
}
.contact-banner .container {
  margin-bottom: 5rem;
}
</style>
