<template>
  <div>
    <h3 class="mrg-b-30">
      <producttitle />
    </h3>
    <div class="mrg-b-30">
      <rating />
    </div>
    <div class="mrg-b-30">
      <productPrice />
    </div>
    <div class="mrg-b-30">
      <available />
    </div>
    <div class="mrg-b-30">
      <productDesc />
    </div>
    <div class="mrg-b-30">
      <size />
    </div>
    <div class="mrg-b-30">
      <colors />
    </div>
    <div class="mrg-b-30">
      <addProduct />
    </div>
    <div class="mrg-b-30">
      <categoriesSingleP />
    </div>
    <div class="mrg-b-30">
      <tags />
    </div>
    <div class="mrg-b-30">
      <shareIcons />
    </div>
  </div>
</template>

<script>
import producttitle from '@/components/partials/listing/product-title.vue'
import productPrice from '@/components/partials/listing/product-price.vue'
import rating from '@/components/partials/listing/rating.vue'
import available from '@/components/partials/listing/available.vue'
import productDesc from '@/components/partials/listing/product-desc.vue'
import size from '@/components/partials/listing/size.vue'
import colors from '@/components/partials/listing/colors.vue'
import addProduct from '@/components/partials/listing/add-product.vue'
import tags from '@/components/partials/listing/tags.vue'
import categoriesSingleP from '@/components/partials/listing/categories-single-p.vue'
import shareIcons from '@/components/partials/listing/share-icons.vue'

export default {
  name: 'ProductDesciption',
  components: {
    producttitle,
    productPrice,
    rating,
    available,
    productDesc,
    size,
    colors,
    addProduct,
    tags,
    categoriesSingleP,
    shareIcons
  }
}
</script>

<style lang="less" scoped>
.disp-flex,
/deep/ .l-size,
.l-rating,
.l-colors,
.l-tags,
.l-share-icons {
  display: flex;
  align-items: center;
  justify-content: center;
}

.mrg-b-30 {
  margin-bottom: 30px;
}

.item-subtitle {
  margin-right: 10px;
  &:last-of-type {
    margin-right: 0;
  }
}

/deep/ .product-price {
  .new-price,
  .price {
    font-size: 20px;
    font-weight: 300;
  }
  .l-rating {
    /deep/ li i::before {
      color: @color-primary-l;
    }
  }
}

/deep/ .product-title {
  font-family: 'playfair';
  font-size: 30px;
  line-height: 36px;
  font-weight: 600;
  color: @color-black;
  text-transform: capitalize;
}

/deep/.sidebar-title {
  font-family: 'poppins';
  font-size: 15px;
  line-height: 19px;
  font-weight: 500;
  color: @color-primary-f;
  text-transform: capitalize;
  opacity: 1;
  padding-bottom: 0;
  margin-right: 30px;
  padding-right: 5px;
  position: relative;
  &::after {
    position: absolute;
    top: 0;
    right: 0;
    content: ':';
    font-weight: 600;
  }
}

/deep/ .l-colors {
  ul {
    display: flex;
    align-items: center;
    justify-content: center;
    li {
      margin-bottom: 0;
      .custom-control-label {
        padding-right: 20px;
      }
    }
  }
  span {
    display: none;
  }
}

/deep/ .l-product-desc {
  p {
    max-width: 800px;
    margin: 0 auto;
  }
}
</style>
