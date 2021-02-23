<template>
  <div class="product-services-list">
    <div v-for="(item, idx) in items" :key="idx" class="product-service-item">
      <div class="item-image">
        <img src="~/assets/images/tick.svg" alt="list-icon" />
      </div>
      <div class="item-info">{{ item.title }}</div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      default() {
        return []
      },
    },
  },

  data() {
    return {}
  },
}
</script>

<style scoped>
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
</style>
