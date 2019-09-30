<template>
  <div class="buttons margin-t-30">
    <b-button type="reset" class="a-dark">
      Reset
    </b-button>
    <b-button type="submit" class="a-dark">
      Filter
    </b-button>
  </div>
</template>

<script>
export default {
  name: 'Buttons'
}
</script>

<style lang="less" scoped>
.buttons {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>
