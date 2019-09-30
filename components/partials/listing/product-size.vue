<template>
  <div class="product-size">
    <b-table :items="items" />
  </div>
</template>

<script>
export default {
  name: 'ProductSize',
  data() {
    return {
      items: [
        { Size: 'S', Bust: '41-42', Waist: '33-38', Hips: '40-42' },
        { Size: 'M', Bust: '43-46', Waist: '38-40', Hips: '43-47' },
        { Size: 'L', Bust: '47-52', Waist: '42-52', Hips: '48-53' },
        { Size: 'XL', Bust: '>52', Waist: '52-58', Hips: '54-60' }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.product-size {
  /deep/ .table td {
    min-width: 250px;
  }
}
</style>
