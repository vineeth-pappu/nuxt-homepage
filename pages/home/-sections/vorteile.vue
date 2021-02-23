<template>
  <section class="benifits-wrapper">
    <div class="container">
      <h4 class="section-title">{{ data.subtitle }}</h4>
      <h1 class="section-header">{{ data.title }}</h1>

      <div class="advantages-wrapper">
        <div class="row">
          <div
            v-for="(item, index) in data.vorteile"
            :key="index"
            class="col-md-3"
          >
            <div class="advantage">
              <div class="advantage-header">
                <div class="advantage-number">{{ index + 1 }}</div>
                <div class="advantage-image">
                  <img :src="item.image.url" alt="advantage" />
                </div>
              </div>
              <h3 class="advantage-title">{{ item.title }}</h3>
              <p class="advantage-content">{{ item.description }}</p>
            </div>
          </div>
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

<style scoped>
.benifits-wrapper {
  background-color: #182540;
  padding: 8rem 0 5.25rem 0;
  color: #fff;
}
.section-title {
  font-family: 'Mulish', sans-serif;
  font-size: 1.125rem;
  font-weight: 700;
  text-align: center;
}
.section-header {
  font-family: 'Lora', serif;
  font-size: 2.625rem;
  text-align: center;
  padding: 1.2rem 0 3.25rem 0;
}
.advantage-title {
  font-family: 'Lora', serif;
  padding: 0.85rem 0 1.65rem 0;
  line-height: 1.5;
  font-size: 1.625rem;
}
.advantage-header {
  display: flex;
  align-items: center;
}
.advantage-number {
  font-size: 5rem;
  font-weight: 600;
  color: rgb(255 255 255 / 16%);
}
.advantage-image {
  margin-left: 0.5rem;
}
.advantage-content {
  font-size: 1.0625rem;
  line-height: 2;
}
</style>
