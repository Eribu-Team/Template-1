<template>
  <div class="products-slider">
    <h2 class="main-title">
      Related products
    </h2>
    <div class="container p-relative">
      <div class="swiper-container">
        <div class="swiper-container-product">
          <div class="swiper-wrapper">
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
            <div class="swiper-slide">
              <singleProduct />
            </div>
          </div>
        </div>
      </div>

      <div class="swiper-button-next2" />
      <div class="swiper-button-prev2" />
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper'
import 'swiper/dist/css/swiper.min.css'
import singleProduct from '@/components/partials/single_product/single-product.vue'

export default {
  name: 'ProductsSlider',
  components: {
    singleProduct
  },
  mounted() {
    const mySwiper = new Swiper('.swiper-container-product', {
      loop: true,
      slidesPerView: 4,
      spaceBetween: 30,
      navigation: {
        nextEl: '.swiper-button-next2',
        prevEl: '.swiper-button-prev2'
      },
      autoplay: {
        delay: 500000
      }
    })
    console.log(mySwiper)
  }
}
</script>

<style lang="less" scoped>
.products-slider {
  margin-bottom: 100px;
  h2 {
    text-align: center;
    margin-bottom: 50px;
  }
  /deep/ img {
    max-width: 100%;
    height: auto;
  }
  /deep/ .single-product-wrapper {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 255px;
    margin: 0 auto;
  }
  .swiper-button-next2,
  .swiper-button-prev2 {
    position: absolute;
    top: 40%;
    transform: translateY(-50%);
    width: 35px;
    height: 35px;
    background-image: none;
    background-color: @color-primary-i;
    border-radius: 50%;
    margin-top: 0;
    cursor: pointer;
    .trans-dur(@m-time);
    &::after {
      position: absolute;
      top: 7px;
      font-family: 'fontello';
      font-size: 30px;
      color: @color-white;
    }
    &:hover {
      background-color: @color-primary-j;
    }
    &:focus {
      outline: none;
    }
  }

  .swiper-button-next2 {
    right: -50px;
    &::after {
      content: '\f105';
      left: 14px;
    }
  }
  .swiper-button-prev2 {
    left: -50px;
    &::after {
      content: '\f104';
      left: 11px;
    }
  }
  /deep/ .youtube-video {
    position: absolute;
    bottom: 20px;
    right: 20px;
    z-index: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 45px;
    height: 45px;
    border-radius: 50%;
    border: 1px solid #f1f1f1;
    background-color: #f1f1f1;
    i::before {
      color: @color-primary-j;
      font-size: 23px;
      .trans-dur(@m-time);
    }
    &:hover {
      i::before {
        color: @color-primary-a;
      }
    }
  }
  /deep/ .modal-dialog {
    max-width: 900px;
    max-height: 500px;
    height: 100%;
    margin: 10% auto;
    .modal-content {
      height: 100%;
    }
    .modal-body {
      background-color: #000;
    }
    .modal-header,
    .modal-footer {
      display: none;
    }
  }
}
</style>
