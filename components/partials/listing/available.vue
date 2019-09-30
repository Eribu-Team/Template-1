<template>
  <div class="l-available">
    <p>Available: <span class="green">In Stock</span></p>
    <!-- <p>Available: <span class="red">Not in Stock</span></!-->
  </div>
</template>

<script>
export default {
  name: 'Available'
}
</script>

<style lang="less" scoped>
.l-available {
  text-align: center;
}
span {
  font-weight: 700;
}
.green {
  color: @color-primary-m;
}
.red {
  color: @color-primary-k;
}
</style>
