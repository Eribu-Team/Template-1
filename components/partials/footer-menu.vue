<template>
  <div>
    <ul class="ul-default-menu">
      <li>
        <nuxt-link to="/" :class="hover">
          Terms & Condition
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/" :class="hover">
          Site map
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/" :class="hover">
          Privacy policy
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/" :class="hover">
          FAQ
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/" :class="hover">
          Affiliate
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'FooterMenu',
  data() {
    return {
      hover: 'horizontal-line-hover'
    }
  }
}
</script>

<style lang="less" scoped>
ul {
  display: inline-flex;
  li {
    a {
      font-weight: 400;
      padding: 0;
      margin: 0 12px;
      color: @color-white;
      text-transform: capitalize;
      &:hover {
        color: @color-primary-i;
      }
    }
  }
}
</style>
