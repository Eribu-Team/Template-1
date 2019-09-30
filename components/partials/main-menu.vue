<template>
  <div>
    <ul class="ul-default-menu">
      <li>
        <nuxt-link to="/" class="vert-line">
          Home
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/listing" class="vert-line">
          Listing
        </nuxt-link>
      </li>
      <li>
        <nuxt-link to="/single-product" class="vert-line">
          Single Product
        </nuxt-link>
      </li>
      <li class="dropdown-parent  vert-line">
        Pages

        <div class="dropdown-children">
          <ul>
            <li><a href="#">About Us</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Faq</a></li>
            <li><a href="#">Page 404</a></li>
          </ul>
        </div>
      </li>
      <li class="dropdown-parent">
        <nuxt-link to="/blog" class="vert-line">
          Blog
        </nuxt-link>
        <div class="dropdown-children">
          <ul>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
          </ul>
        </div>
      </li>
      <li class="dropdown-parent">
        <nuxt-link to="/collection" class="vert-line">
          Collection
        </nuxt-link>
        <div class="dropdown-children">
          <ul>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
            <li><a href="#">lorem</a></li>
          </ul>
        </div>
      </li>
      <li>
        <nuxt-link to="/example" class="vert-line">
          Example
        </nuxt-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Menu'
}
</script>

<style lang="less" scoped>
ul {
  display: inline-flex;
}

.vert-line {
  position: relative;
  &::before {
    position: absolute;
    width: 2px;
    height: 0;
    top: -41px;
    left: 50%;
    transform: translateX(-50%);
    content: '';
    background: @color-primary-a;
    visibility: hidden;
    opacity: 0;
    .trans-dur(@m-time);
  }
  &:hover {
    color: @color-primary-a;
    &::before {
      visibility: visible;
      opacity: 1;
      height: 40px;
    }
  }
}

.nuxt-link-exact-active {
  color: @color-primary-a;
  &::before {
    visibility: visible;
    opacity: 1;
    height: 40px;
  }
}
</style>
