<template>
  <div class="default-tabs">
    <b-tabs>
      <b-tab
        title="Description"
        title-link-class="horizontal-line-hover"
        active
      >
        <div class="max-w-700">
          <h3>Details</h3>
          <productDesc />
        </div>
      </b-tab>
      <b-tab title="Size Guide" title-link-class="horizontal-line-hover">
        <productSize />
      </b-tab>
      <b-tab title="Shipping" title-link-class="horizontal-line-hover">
        <p>*Estimated Shipping times throughout North America</p>
        <productShipping />
        <p>
          Exclude all mexico and International orders.Please see contact page
          for International policies.
        </p>
      </b-tab>
      <b-tab title="Reviews" title-link-class="horizontal-line-hover">
        <singleOpinion />
        <writeOpinion />
      </b-tab>
    </b-tabs>
  </div>
</template>

<script>
import productDesc from '@/components/partials/listing/product-desc.vue'
import productSize from '@/components/partials/listing/product-size.vue'
import productShipping from '@/components/partials/listing/product-shipping.vue'
import singleOpinion from '@/components/partials/opinions/single-opinion.vue'
import writeOpinion from '@/components/partials/opinions/write-opinion.vue'

export default {
  name: 'ProductTabs',
  components: {
    productDesc,
    productSize,
    productShipping,
    singleOpinion,
    writeOpinion
  }
}
</script>

<style lang="less" scoped>
.default-tabs {
  width: 100%;
}
.max-w-700 {
  max-width: 700px;
  margin: 0 auto;
}
/deep/ .l-product-desc {
  text-align: left;
}
/deep/ h3 {
  color: @color-black;
  font-family: 'playfair';
  font-size: 24px;
  line-height: 28px;
  margin-bottom: 30px;
  text-align: left;
}
</style>
