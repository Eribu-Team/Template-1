<template>
  <div class="l-images">
    <ul class="images-out">
      <li>
        <a href="#">
          <b-img src="~assets/img/listing/product-1.jpg" alt="image" />
        </a>
      </li>
      <li>
        <a href="#">
          <b-img src="~assets/img/listing/product-3.jpg" alt="image" />
        </a>
      </li>
      <li class="active">
        <a href="#">
          <b-img src="~assets/img/listing/product-12.jpg" alt="image" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Size'
}
</script>

<style lang="less" scoped>
.images-out {
  display: flex;
  justify-content: center;
  align-items: center;
  padding-left: 0;
  list-style-type: none;
  li {
    margin: 0 5px;
    &:first-of-type {
      margin-left: 0;
    }
    &:last-of-type {
      margin-right: 0;
    }
    a {
      display: block;
      width: 33px;
      height: 33px;
      img {
        max-width: 100%;
        height: auto;
        border-radius: 50%;
        opacity: 0.6;
        .trans-dur(@m-time);
      }
    }
    &.active,
    &:hover {
      img {
        opacity: 1;
      }
    }
  }
}
</style>
