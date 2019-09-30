<template>
  <div>
    <div class="container-short">
      <slider />
      <div class="product-desc">
        <ProductDesciption />
        <div class="disp-flex">
          <productTabs />
        </div>
        <div />
      </div>
    </div>
    <productsSlider />
  </div>
</template>

<script>
import slider from '@/components/partials/single_product/slider.vue'
import ProductDesciption from '@/components/partials/single_product/product-desciption.vue'
import productTabs from '@/components/partials/single_product/product-tabs.vue'
import productsSlider from '@/components/partials/listing/products-slider.vue'

export default {
  layout: 'light',
  components: {
    slider,
    ProductDesciption,
    productTabs,
    productsSlider
  }
}
</script>

<style lang="less" scoped>
.product-desc {
  margin: 50px auto;
}
/deep/ .default-tabs {
  margin-top: 100px;
  margin-bottom: 100px;
}
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
