<template>
  <div class="w-100">
    <div class="outside-gallery">
      <div class="swiper-container">
        <div class="swiper-wrapper">
          <div class="swiper-slide">
            <b-img src="~assets/img/single_product/img-13.jpg" />
          </div>
          <div class="swiper-slide">
            <b-img src="~assets/img/single_product/img-14.jpg" />
          </div>
          <div class="swiper-slide">
            <b-img src="~assets/img/single_product/img-15.jpg" />
          </div>
        </div>
        <div class="swiper-button-next" />
        <div class="swiper-button-prev" />
        <button v-b-modal.modal-youtube class="youtube-video" href="#">
          <i class="icon-youtube-play" />
        </button>
        <b-modal id="modal-youtube" class="youtube">
          <iframe
            autoplay
            width="100%"
            height="100%"
            src="https://www.youtube.com/embed/2x5lDFEKZ0s?autoplay=1"
            frameborder="0"
            allow="accelerometer; autoplay; encrypted-media;
          gyroscope; picture-in-picture"
            allowfullscreen
          />
        </b-modal>
      </div>
    </div>
  </div>
</template>

<script>
import Swiper from 'swiper'
import 'swiper/dist/css/swiper.min.css'

export default {
  name: 'Slider',

  mounted() {
    const mySwiper = new Swiper('.swiper-container', {
      loop: true,
      navigation: {
        nextEl: '.swiper-button-next',
        prevEl: '.swiper-button-prev'
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
.outside-gallery {
  max-width: 920px;
  margin: 0 auto;
}
img {
  max-width: 100%;
  height: auto;
}
.swiper-button-next,
.swiper-button-prev {
  transform: translateY(-50%);
  width: 35px;
  height: 35px;
  background-image: none;
  background-color: @color-primary-i;
  border-radius: 50%;
  margin-top: 0;
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
}

.swiper-button-next {
  &::after {
    content: '\f105';
    left: 14px;
  }
}
.swiper-button-prev {
  &::after {
    content: '\f104';
    left: 11px;
  }
}
.youtube-video {
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
</style>
