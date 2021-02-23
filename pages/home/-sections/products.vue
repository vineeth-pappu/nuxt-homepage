<template>
  <section class="products-wrapper">
    <div
      v-for="(product, index) in data.services"
      :key="index"
      class="product-details-wrapper"
    >
      <div class="product-details">
        <h1 class="product-title">{{ product.title }}</h1>
        <div class="product-services-list">
          <div
            v-for="(item, idx) in product.list"
            :key="idx"
            class="product-service-item"
          >
            <div class="item-image">
              <img src="~/assets/images/tick.svg" alt="list-icon" />
            </div>
            <div class="item-info">{{ item.title }}</div>
          </div>
        </div>
        <div class="product-footer">
          <div class="product-footer-item">
            <app-button-primary>{{ product.button }}</app-button-primary>
          </div>
          <div class="product-footer-item" v-if="product.price">
            <div class="product-price">
              <div class="price-tag">
                <img :src="data.price_label_image" alt="tag" />
                price
              </div>
              <div class="price-amount">{{ product.price }}</div>
            </div>
          </div>
        </div>
      </div>
      <div class="product-image">
        <img :src="product.image.url" alt="product-image" />
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
.product-service-item {
  display: flex;
  padding: 0.5rem;
  margin: 1rem 0;
  font-size: 1.0625rem;
  color: #182540;
}
.item-image {
  margin-right: 1.2rem;
}
.product-image img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
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
