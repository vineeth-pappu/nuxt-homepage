<template>
  <section class="products-wrapper">
    <div
      v-for="(product, index) in data.services"
      :key="index"
      class="product-details-wrapper"
    >
      <div class="product-details">
        <h1 class="product-title">{{ product.title }}</h1>
        <services :items="product.list"></services>
        <product-footer
          :product="product"
          :price-tag-img="data.price_label_image"
        ></product-footer>
      </div>
      <div class="product-image">
        <img :src="product.image.url" alt="product-image" />
      </div>
    </div>
  </section>
</template>

<script>
import Services from '@/components/home/products/services'
import ProductFooter from '@/components/home/products/product-footer'

export default {
  components: {
    Services,
    ProductFooter,
  },

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
.product-details-wrapper {
  display: flex;
}
.product-details-wrapper:nth-child(2) {
  flex-direction: row-reverse;
}
.product-details,
.product-image {
  width: 50%;
}
.product-details {
  padding: 5rem;
  padding-right: 2rem;
  padding-bottom: 4rem;
}
.product-title {
  font-family: 'Lora', serif;
  color: #182540;
  font-weight: 500;
  padding-bottom: 1.25rem;
}
.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
