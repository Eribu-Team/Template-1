<template>
  <div class="header-menu">
    <div class="container">
      <nav class="top-nav">
        <logo />
        <mainmenu />
        <shop-nav />
      </nav>
    </div>
  </div>
</template>

<script>
import logo from '@/components/partials/logo.vue'
import mainmenu from '@/components/partials/main-menu.vue'
import shopNav from '@/components/partials/shop-nav.vue'

export default {
  name: 'TopNav',
  components: {
    logo,
    mainmenu,
    shopNav
  }
}
</script>

<style lang="less" scoped>
.header-menu {
  padding-top: 20px;
  padding-bottom: 20px;
}
.top-nav {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
