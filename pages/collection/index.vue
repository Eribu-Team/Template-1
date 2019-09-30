<template>
  <div>
    <h3 class="page-title">
      {{ items[1].text }}
    </h3>
    <b-breadcrumb :items="items" />
    <div class="bg-color-light">
      <b-img
        class="d-block-mrg-0-auto"
        src="~assets/img/listing/shop-shoes.jpg"
      />
    </div>
    <div class="text-center">
      <h1>COLLECTION</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Blog',
  data() {
    return {
      items: [
        {
          text: 'Home',
          href: '/'
        },
        {
          text: 'Collection',
          href: '/collection'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped></style>
