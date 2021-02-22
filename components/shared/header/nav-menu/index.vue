<template>
  <div class="nav-menu-wapper">
    <app-header-nav-menu-item v-for="(link, index) in pageLinks" :key="index">
      {{ link.title }}
    </app-header-nav-menu-item>
    <app-header-nav-menu-item>
      <app-button-primary> {{ buttonText }} </app-button-primary>
    </app-header-nav-menu-item>
  </div>
</template>

<script>
export default {
  props: {
    pageLinks: {
      type: Array,
      default() {
        return []
      },
    },
    buttonText: {
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
.nav-menu-wapper {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
