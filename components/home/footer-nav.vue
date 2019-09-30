<template>
  <div class="footer dark-mask">
    <div class="container">
      <div class="footer-ins">
        <div class="disp-flex">
          <socialIcons />
          <footer-menu />
          <payments />
        </div>
        <div class="copyright">
          <a href="/">
            <logoWhite />
          </a>
          <p>All rights Reserved @Darek -M 2019</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import socialIcons from '@/components/partials/social-icons.vue'
import footerMenu from '@/components/partials/footer-menu.vue'
import payments from '@/components/partials/payments.vue'
import logoWhite from '@/components/partials/logo-white.vue'

export default {
  name: 'FooterNav',
  components: {
    socialIcons,
    footerMenu,
    payments,
    logoWhite
  }
}
</script>

<style lang="less" scoped>
.footer {
  background-image: url('~assets/img/footer/footer-3.jpg');
  background-position: top;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 100%;
  .footer-ins {
    position: relative;
    z-index: 1;
    padding-top: 120px;
    padding-bottom: 120px;
  }
  .disp-flex {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
  .copyright {
    margin-top: 50px;
    display: flex;
    justify-content: center;
    align-items: center;
    color: @color-white;
    p {
      margin-left: 20px;
    }
  }
}
</style>
