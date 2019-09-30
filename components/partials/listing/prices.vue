<template>
  <div>
    <h2 class="sidebar-title text-t-capitalize">
      Price
    </h2>
    <div>
      <label for="range-2" />
      <b-form-input
        id="range-2"
        v-model="value"
        type="range"
        min="0"
        max="2000"
        step="0.1"
      />
      <div class="range-value">
        $
        {{ value }}
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Prices',
  data() {
    return {
      value: '2'
    }
  }
}
</script>

<style lang="less" scoped>
.range-value {
  font-size: 16px;
  line-height: 24px;
}
</style>
