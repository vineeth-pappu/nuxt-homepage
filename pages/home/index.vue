<template>
  <div>
    <h1>---- {{ data.title }} ---------</h1>
    <main-banner></main-banner>
    <referenzen></referenzen>
    <vorteile></vorteile>
    <products></products>
    <contact-banner></contact-banner>
  </div>
</template>

<script>
import MainBanner from './-sections/main-banner'
import Referenzen from './-sections/referenzen'
import Vorteile from './-sections/vorteile'
import Products from './-sections/products'
import ContactBanner from './-sections/contact-banner'

export default {
  components: {
    MainBanner,
    Referenzen,
    Vorteile,
    Products,
    ContactBanner,
  },

  async asyncData({ $axios }) {
    const { data } = await $axios.get('/mock-data/payload-shared.json')
    console.log('data-----------------', data)
    return { data }
  },

  data() {
    return {}
  },
}
</script>

<style></style>
