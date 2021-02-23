<template>
  <section class="products-wrapper">
    <div v-for="(product, index) in data.services" :key="index" class="row">
      <div class="col-md-6">
        <div class="product-details">
          <h1>{{ product.title }}</h1>
        </div>
      </div>
      <div class="col-md-6">
        <div class="product-image">
          <img :src="product.image.url" alt="" />
        </div>
      </div>
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

<style></style>
