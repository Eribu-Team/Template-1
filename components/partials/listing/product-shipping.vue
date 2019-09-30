<template>
  <div class="product-shipping">
    <b-table :items="items" />
  </div>
</template>

<script>
export default {
  name: 'ProductShipping',
  data() {
    return {
      items: [
        {
          'Shipping Type': 'Standard Ground',
          Cost: 'Free',
          'Estimated Time': 'Product will delivery in 3-5 business days'
        },
        {
          'Shipping Type': 'Standard Ground',
          Cost: 'Free',
          'Estimated Time': 'Product will delivery in 3-5 business days'
        },
        {
          'Shipping Type': 'Standard Ground',
          Cost: 'Free',
          'Estimated Time': 'Product will delivery in 3-5 business days'
        },
        {
          'Shipping Type': 'Standard Ground',
          Cost: 'Free',
          'Estimated Time': 'Product will delivery in 3-5 business days'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.product-shipping {
  margin-top: 20px;
  margin-bottom: 20px;
  /deep/ .table td {
    min-width: 200px;
    &:last-of-type {
      min-width: 500px;
    }
  }
}
</style>
