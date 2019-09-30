<template>
  <div>
    <top-nav />
    <nuxt />
    <footer-nav />
  </div>
</template>

<script>
import topNav from '@/components/home/top-nav.vue'
import footerNav from '@/components/home/footer-nav.vue'

export default {
  components: {
    topNav,
    footerNav
  }
}
</script>

<style lang="less"></style>
