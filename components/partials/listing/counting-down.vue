<template>
  <div class="l-counting-down disp-flex">
    <div class="l-counting">
      <div class="l-counting-ins">
        <span>00</span>
        <p>Days</p>
      </div>
    </div>
    <div class="l-counting">
      <div class="l-counting-ins">
        <span>00</span>
        <p>Hours</p>
      </div>
    </div>
    <div class="l-counting">
      <div class="l-counting-ins">
        <span>0</span>
        <p>mins</p>
      </div>
    </div>
    <div class="l-counting">
      <div class="l-counting-ins">
        <span>0</span>
        <p>secs</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CountingDown'
}
</script>

<style lang="less" scoped>
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: center;
}
.l-counting-down {
  .l-counting {
    background-color: @color-white;
    margin: 0 5px;
    text-align: center;
    color: @color-black;
    padding: 7px 5px;
    &:first-of-type {
      margin-left: 0;
    }
    &:last-of-type {
      margin-right: 0;
    }
    &-ins {
      width: 40px;
      height: 40px;
    }
  }
  span {
    font-size: 25px;
    display: block;
    line-height: 31px;
  }
  p {
    font-size: 12px;
    line-height: 12px;
  }
}
</style>
