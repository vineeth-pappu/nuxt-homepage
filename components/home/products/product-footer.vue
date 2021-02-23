<template>
  <div class="product-footer">
    <div class="product-footer-item">
      <app-button-primary>{{ product.button }}</app-button-primary>
    </div>
    <div v-if="product.price" class="product-footer-item">
      <div class="product-price">
        <div class="price-tag">
          <img :src="priceTagImg" alt="tag" />
          price
        </div>
        <div class="price-amount">{{ product.price }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      default() {
        return {}
      },
    },
    priceTagImg: {
      type: String,
      default: '',
    },
  },

  data() {
    return {}
  },
}
</script>

<style scoped>
.product-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-top: 2rem;
}
.product-footer-item {
  /* width: 50%; */
  flex: 1;
}
.product-price {
  padding-left: 1rem;
}
.price-tag {
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 7px;
  position: relative;
  display: flex;
  align-items: center;
  height: 25px;
  color: #fff;
  padding-left: 0.85rem;
}
.price-tag img {
  position: absolute;
  z-index: -1;
  left: 0;
}
.price-amount {
  font-family: 'Lora', serif;
  font-size: 2.625rem;
  font-weight: 500;
  color: #182540;
}
.product-footer .app-btn:hover {
  letter-spacing: 2px;
}
</style>
