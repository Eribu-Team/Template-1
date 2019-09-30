<template>
  <div>
    <ul class="ul-default-menu">
      <li>
        <a href="#">
          <i class="icon-search" />
        </a>
      </li>
      <li class="dropdown-parent">
        <a href="#" class="a-menu">
          <i class="icon-user-o" />
        </a>
        <div class="dropdown-children">
          <ul>
            <li><a href="#">My Account</a></li>
            <li><a href="#">Wishlist</a></li>
            <li><a href="#">Checkout</a></li>
            <li><a href="#">Shopcart</a></li>
            <li><a href="/login">Login</a></li>
          </ul>
        </div>
      </li>
      <li>
        <a href="#" class="p-relative">
          <i class="icon-basket" />
          <span>3</span>
        </a>
      </li>
      <li>
        <a href="#">
          <i class="icon-sliders" />
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'ShopNav'
}
</script>

<style lang="less" scoped>
.ul-default-menu {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0;
  margin: 0;
  list-style: none;
  li {
    a {
      i {
        &::before {
          font-size: 18px;
          color: @color-primary;
          .trans-dur(@m-time);
        }
      }
      &:hover {
        i::before {
          color: @color-primary-a;
        }
      }
      span {
        position: absolute;
        top: -11px;
        right: -11px;
        background: @color-primary-k;
        width: 18px;
        height: 18px;
        border-radius: 50%;
        color: #fff;
        text-align: center;
        font-size: 11px;
        line-height: 18px;
      }
    }
  }
}
.dropdown-parent {
  .dropdown-children {
    width: 150px;
    align-items: flex-start;
    left: auto;
    right: -50%;
    ul {
      padding: 30px 20px;
    }
  }
}
</style>
