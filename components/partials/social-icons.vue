<template>
  <div class="social icons disp-flex">
    <a href="#">
      <i class="icon-facebook" />
    </a>
    <a href="#">
      <i class="icon-instagram" />
    </a>
    <a href="#">
      <i class="icon-twitter" />
    </a>
    <a href="#">
      <i class="icon-youtube-play" />
    </a>
  </div>
</template>

<script>
export default {
  name: 'SocialIcons'
}
</script>

<style lang="less" scoped>
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: center;
}
a {
  margin-right: 20px;
  &:last-of-type {
    margin-right: 0;
  }
  i {
    &::before {
      color: @color-white;
      .trans-dur(@m-time);
      font-size: 17px;
      display: block;
    }
  }
  &:hover {
    i::before {
      color: @color-primary-i;
    }
  }
}
</style>
