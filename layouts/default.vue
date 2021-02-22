<template>
  <div>
    <app-header :data="content.section_navbar"></app-header>
    <Nuxt />
    <app-footer></app-footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: {},
    }
  },

  async fetch() {
    const { data } = await this.$nuxt.context.$axios.get(
      '/mock-data/payload-shared.json'
    )
    this.content = data
  },
}
</script>

<style></style>
