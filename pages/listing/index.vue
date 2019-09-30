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
    <div class="container-short">
      <div class="container-short-ins">
        <div class="container-short-ins-left">
          <div class="margin-b-60">
            <categories />
          </div>
          <div class="margin-b-30">
            <filters />
          </div>
          <div class="margin-b-30">
            <prices />
          </div>
          <div class="margin-b-30">
            <size />
          </div>
          <div class="margin-b-30">
            <colors />
          </div>
          <buttons />
        </div>
        <div class="container-short-ins-right">
          <quantity-product />
          <products-listing />
          <pagination />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import categories from '@/components/partials/listing/categories.vue'
import filters from '@/components/partials/listing/filters.vue'
import prices from '@/components/partials/listing/prices.vue'
import size from '@/components/partials/listing/size.vue'
import colors from '@/components/partials/listing/colors.vue'
import buttons from '@/components/partials/listing/buttons.vue'
import quantityProduct from '@/components/partials/listing/quantity-product.vue'
import productsListing from '@/components/partials/listing/products-listing.vue'
import pagination from '@/components/partials/other/pagination.vue'

export default {
  components: {
    categories,
    filters,
    prices,
    size,
    colors,
    buttons,
    quantityProduct,
    productsListing,
    pagination
  },
  data() {
    return {
      items: [
        {
          text: 'Home',
          href: '/'
        },
        {
          text: 'Shop',
          href: '/listing'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.container-short-ins-left {
  margin-bottom: 50px;
  /deep/ .l-colors {
    li {
      justify-content: space-between;
      margin-left: 0;
      margin-right: 0;
    }
  }
}
</style>
