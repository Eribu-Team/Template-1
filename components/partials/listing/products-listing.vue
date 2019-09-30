<template>
  <div class="product-listing disp-grid">
    <singleProduct />
  </div>
</template>

<script>
import singleProduct from '@/components/partials/single_product/single-product.vue'

export default {
  name: 'ProductsListing',
  components: {
    singleProduct
  }
}
</script>

<style lang="less" scoped>
.disp-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}
.product-listing {
  /deep/ .single-product {
    margin-bottom: 60px;
    &:nth-of-type(3n + 1) {
      margin-right: auto;
      margin-left: 0;
    }

    &:nth-of-type(3n + 2) {
      margin-left: auto;
      margin-right: auto;
    }

    &:nth-of-type(3n + 3) {
      margin-left: auto;
      margin-right: 0;
    }
  }
}
</style>
