<template>
  <div>
    <main-banner :data="data.section_head"></main-banner>
    <referenzen></referenzen>
    <vorteile :data="data.section_vorteile"></vorteile>
    <products :data="data.section_services"></products>
    <contact-banner :data="data.section_contact"></contact-banner>
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
    const { data } = await $axios.get('/mock-data/payload-home.json')
    // console.log({ data })
    return { data }
  },

  data() {
    return {}
  },
}
</script>

<style></style>
