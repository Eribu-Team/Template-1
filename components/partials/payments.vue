<template>
  <div class="bank-payments disp-flex">
    <a href="">
      <b-img src="~/assets/img/footer/payment-1.png" />
    </a>
    <a href="">
      <b-img src="~/assets/img/footer/payment-2.png" />
    </a>
    <a href="">
      <b-img src="~/assets/img/footer/payment-3.png" />
    </a>
  </div>
</template>

<script>
export default {
  name: 'Payments'
}
</script>

<style lang="less" scoped>
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: center;
}

a {
  margin-right: 10px;
  &:last-of-type {
    margin-right: 0;
  }
}
</style>
