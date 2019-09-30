<template>
  <div class="l-size">
    <h2 class="sidebar-title text-t-capitalize">
      Size
    </h2>
    <div class="size-checkbox">
      <ul class="sizes-out">
        <li><a href="#">S</a></li>
        <li><a href="#">M</a></li>
        <li><a href="#">L</a></li>
        <li><a href="#">XL</a></li>
        <li class="active">
          <a href="#">XXL</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Size'
}
</script>

<style lang="less" scoped>
.sizes-out {
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
      display: flex;
      align-items: center;
      justify-content: center;
      width: 33px;
      height: 33px;
      color: @color-primary-i;
      border: 1px solid @color-white;
      border-radius: 50%;
      background-color: @color-primary-h;
      &:hover {
        border-color: @color-primary-i;
        color: @color-black;
      }
    }
    &.active {
      a {
        border-color: @color-primary-i;
        color: @color-black;
      }
    }
  }
}
</style>
