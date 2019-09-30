<template>
  <div class="single-product">
    <div class="single-product-wrapper">
      <div class="single-product-item dark-mask">
        <b-img src="~assets/img/listing/product-4.jpg" alt="image" />
        <div class="product-promo circle">
          <p>-30%</p>
        </div>
        <div class="product-overlay">
          <button
            v-b-tooltip.hover.right
            v-b-modal="'product-modal'"
            title="quick view"
            class="quick-icon"
          >
            <i class="icon-eye" />
          </button>
          <button
            v-b-tooltip.hover.right
            href="#"
            class="quick-icon"
            title="add to wishlist"
          >
            <i class="icon-heart-empty" />
          </button>
          <button
            v-b-tooltip.hover.right
            href="#"
            class="quick-icon"
            title="add to compare"
          >
            <i class="icon-exchange" />
          </button>
        </div>
      </div>
      <div class="product-details">
        <div class="product-details-fadeOut">
          <div class="margin-b-3">
            <productTitle />
          </div>
          <div class="product-rating margin-b-3">
            <rating />
          </div>
          <div class="margin-b-3">
            <ProductPrice />
          </div>
        </div>
        <div class="product-details-fadeOut-details">
          <div class="margin-b-15">
            <colors />
          </div>
          <a href="#" class="a-dark">
            View Details
          </a>
        </div>
      </div>
    </div>
    <!-- MODAL START -->
    <div>
      <b-modal id="product-modal">
        <div class="inside">
          <div class="left">
            <slider />
          </div>
          <div class="right">
            <productDescription />
          </div>
        </div>
      </b-modal>
    </div>
    <!-- MODAL END -->
  </div>

  <!-- Wyjaśnienie:
  1. do klasy product-promo możesz dodać klasy: circle, rectangle i ribbon
  ___rectangle i ribbon jest sztywne, tam idzie maks ilość znaków 4, np. -30%
  2. do klasy single-product-item możesz dodać klasy: dark-mask, change-image i zoom-image
  ___dark-mask może być łączone z change-image lub zoom-image
  ___change-image potrzebuje drugie zdjęcia
  3. do diva product-details-fadeOut-details możesz wstawić komponent z <size /> lub <colors /> lub <images />
  ___, dlatego komponenty poniżej są zakomentowane
  4. Na stronie http://127.0.0.1:3000/example masz pełny obraz, przykład tego co powyżej napisałem:) -->
</template>

<script>
import ProductPrice from '@/components/partials/listing/product-price.vue'
import productTitle from '@/components/partials/listing/product-title.vue'
import colors from '@/components/partials/listing/colors.vue'
// import size from '@/components/partials/listing/size.vue'
// import countingDown from '@/components/partials/listing/counting-down.vue'
// import images from '@/components/partials/listing/images.vue'
import rating from '@/components/partials/listing/rating.vue'
import slider from '@/components/partials/single_product/slider.vue'
import productDescription from '@/components/partials/single_product/product-desciption.vue'

export default {
  name: 'ProductsListing',
  components: {
    ProductPrice,
    productTitle,
    colors,
    // size,
    // countingDown,
    // images,
    rating,
    slider,
    productDescription
  }
}
</script>

<style lang="less" scoped>
/deep/ .modal-dialog {
  max-width: 800px;
  min-height: 200px;
  margin: 5% auto;

  .inside {
    .left {
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 40px;
    }
  }

  .mrg-b-30 {
    margin-bottom: 20px;
  }

  .swiper-slide {
    width: 100%;
  }

  .modal-content {
    height: 100%;
  }

  .modal-body {
    background-color: @color-white;
    padding: 0 33.7px 50px;
  }

  .modal-header {
    border: none;
    padding: 0;

    .close {
      padding: 5px 10px;
      margin: 0;
      background-color: @color-black;
      color: @color-white;
      opacity: 1;
      .trans-dur(@m-time);

      &:hover {
        background-color: @color-primary-c;
      }
    }
  }

  .modal-footer {
    display: none;
  }

  .youtube-video {
    display: none;
  }
  /deep/ .custom-control-label {
    padding-right: 20px;
  }
}

.product-details {
  /deep/ .product-title {
    font-size: 14px;
    font-weight: 300;
  }
  /deep/ .listing-colors {
    ul {
      display: flex;
      align-items: center;
      justify-content: center;
      li {
        margin-bottom: 0;
      }
      .custom-control-input {
        width: 15px;
        height: 18px;
      }
      .custom-control-label {
        padding-left: 0;
        width: 15px;
        color: transparent;
        pointer-events: none;
        &::before {
          border: none;
          width: 15px;
          height: 18px;
        }
      }
    }
    span,
    .sidebar-title {
      display: none;
    }
  }
  /deep/ .l-size {
    .sidebar-title {
      display: none;
    }
  }
  /deep/ .product-rating {
    span {
      display: none;
    }
  }
}
</style>
