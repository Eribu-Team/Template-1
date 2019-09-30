<template>
  <div class="l-share-icons">
    <h2 class="sidebar-title text-t-capitalize">
      Share
    </h2>
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
    </div>
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
  display: flex;
  align-items: center;
  justify-content: center;
  width: 38px;
  height: 38px;
  border-radius: 50%;
  border: 1px solid @color-primary-h;
  margin: 0 5px;
  background-color: @color-primary-h;
  &:first-of-type {
    margin-left: 0;
  }
  &:last-of-type {
    margin-right: 0;
  }
  i {
    &::before {
      color: @color-primary-j;
      .trans-dur(@m-time);
      font-size: 17px;
      display: block;
    }
  }
  &:hover {
    border-color: @color-primary-n;
    background-color: @color-white;
  }
}
</style>
