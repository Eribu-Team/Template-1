<template>
  <div>
    <h3 class="page-title">
      {{ items[1].text }}
    </h3>
    <b-breadcrumb :items="items" />
    <div class="bg-color-light">
      <b-img
        class="d-block-mrg-0-auto"
        src="~assets/img/listing/shop-shoes.jpg"
      />
    </div>
    <div class="margin-t-b-100 container-short">
      <div class="default-tabs login">
        <b-tabs>
          <b-tab title="Login" title-link-class="" active>
            <form>
              <b-form-input type="email" placeholder="Email" />
              <b-form-input type="password" placeholder="Password" />
              <div class="disp-flex">
                <b-form-checkbox
                  id="checkbox-1"
                  name="checkbox-1"
                  value="accepted"
                >
                  Remember me
                </b-form-checkbox>
                <a href="#">Forgot password?</a>
              </div>
              <button href="#" type="submit" class="a-dark">
                Login
              </button>
            </form>
          </b-tab>
          <b-tab title="Register" title-link-class="">
            <form>
              <b-form-input type="text" placeholder="Username" />
              <b-form-input type="email" placeholder="Email" />
              <b-form-input type="password" placeholder="Password" />
              <b-form-input type="password" placeholder="Confirm password" />
              <button href="#" type="submit" class="a-dark">
                Register
              </button>
            </form>
          </b-tab>
        </b-tabs>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Login',
  data() {
    return {
      items: [
        {
          text: 'Home',
          href: '/'
        },
        {
          text: 'Login',
          href: '/login'
        }
      ]
    }
  }
}
</script>

<style lang="less" scoped>
.login {
  max-width: 540px;
  width: 100%;
  margin-left: auto;
  margin-right: auto;
}
.custom-control {
  display: inline-block;
  width: auto;
}
.disp-flex {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-top: 15px;
}
a:not(.a-dark),
/deep/ .custom-control-label {
  color: @color-primary-j;
  .trans-dur(@m-time);
  &:hover {
    color: @color-black;
  }
}
.a-dark {
  margin-top: 30px;
}
</style>
