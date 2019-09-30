<template>
  <div class="quantity-product disp-flex">
    <div>
      <a href="#">
        <i class="icon-th" />
      </a>
      <a href="#">
        <i class="icon-th-list" />
      </a>
    </div>
    <div>
      <span>Showing 1-15 of 69 products</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'QuantityProduct'
}
</script>

<style lang="less" scoped>
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.quantity-product {
  margin-bottom: 30px;
  a {
    display: inline-block;
    i {
      display: inline-block;
      &::before {
        font-size: 20px;
        color: @color-black;
        .trans-dur(@m-time);
      }
    }
    &:nth-of-type(1) {
      margin-right: 10px;
    }
    &:hover {
      i::before {
        color: @color-primary-a;
      }
    }
  }
  span {
    display: block;
    color: @color-primary-a;
  }
}
</style>
