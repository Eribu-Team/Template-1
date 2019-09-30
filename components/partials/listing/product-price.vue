<template>
  <div class="l-product-price">
    <div class="product-price margin-b-3">
      <span class="new-price">$383</span>
      <span class="price">$499</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductTitle'
}
</script>

<style lang="less" scoped>
.product-price {
  display: flex;
  align-items: center;
  justify-content: center;

  span {
    display: block;
  }

  .new-price {
    color: @color-black;
    font-weight: 500;
  }

  .price {
    margin-left: 10px;
    text-decoration: line-through;
  }
}
</style>
