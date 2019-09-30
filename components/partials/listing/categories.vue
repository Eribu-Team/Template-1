<template>
  <div>
    <h2 class="sidebar-title">
      Categories
    </h2>
    <div role="tablist">
      <b-card no-body>
        <b-card-header header-tag="header" role="tab">
          <b-button v-b-toggle.accordion-1 block href="#">
            Shirts
          </b-button>
        </b-card-header>
        <b-collapse
          id="accordion-1"
          accordion="my-accordion"
          role="tabpanel"
          class="open-collapse"
        >
          <b-card-body>
            <ul>
              <li><a href="#">Calvin Klein</a></li>
              <li><a href="#">HiM</a></li>
              <li><a href="#">Nautica</a></li>
              <li><a href="#">Bosch</a></li>
            </ul>
          </b-card-body>
        </b-collapse>
      </b-card>

      <b-card no-body>
        <b-card-header header-tag="header" role="tab">
          <b-button v-b-toggle.accordion-2 block href="#">
            Jeans
          </b-button>
        </b-card-header>
        <b-collapse
          id="accordion-2"
          accordion="my-accordion"
          role="tabpanel"
          class="open-collapse"
        >
          <b-card-body>
            <ul>
              <li><a href="#">Levi's</a></li>
              <li><a href="#">Diesel</a></li>
              <li><a href="#">Calvin Klein</a></li>
              <li><a href="#">Armani</a></li>
              <li><a href="#">Nostrum</a></li>
            </ul>
          </b-card-body>
        </b-collapse>
      </b-card>

      <b-card no-body>
        <b-card-header header-tag="header" role="tab">
          <b-button v-b-toggle.accordion-3 block href="#">
            Watch
          </b-button>
        </b-card-header>
        <b-collapse
          id="accordion-3"
          accordion="my-accordion"
          role="tabpanel"
          class="open-collapse"
        >
          <b-card-body>
            <ul>
              <li><a href="#">Titan</a></li>
              <li><a href="#">Omega SA</a></li>
              <li><a href="#">Breguet</a></li>
              <li><a href="#">Seiko</a></li>
              <li><a href="#">Rolex</a></li>
            </ul>
          </b-card-body>
        </b-collapse>
      </b-card>

      <b-card no-body>
        <b-card-header header-tag="header" role="tab">
          <b-button v-b-toggle.accordion-4 block href="#">
            Shoes
          </b-button>
        </b-card-header>
        <b-collapse
          id="accordion-4"
          accordion="my-accordion"
          role="tabpanel"
          class="open-collapse"
        >
          <b-card-body>
            <ul>
              <li><a href="#">Reebok</a></li>
              <li><a href="#">Jordan</a></li>
              <li><a href="#">Vans</a></li>
              <li><a href="#">Converse</a></li>
              <li><a href="#">Puma</a></li>
            </ul>
          </b-card-body>
        </b-collapse>
      </b-card>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Categories'
}
</script>

<style lang="less" scoped>
.card {
  background-color: transparent;
  border: none;
  border-radius: 0;
  .card-header {
    padding: 0;
    margin-bottom: 0;
    background-color: transparent;
    border-bottom: none;
    border-radius: 0;
    &:focus {
      outline: none;
    }
    a {
      position: relative;
      display: block;
      font-size: 16px;
      line-height: 20px;
      color: @color-primary-c;
      text-align: left;
      padding: 14px 0;
      border: none;
      background-color: transparent;
      border-bottom: 1px solid @color-primary-d;
      cursor: pointer;
      &:focus,
      &:active {
        box-shadow: none !important;
      }
      &:active {
        color: @color-primary-c;
        background-color: transparent;
        border: none;
        border-bottom: 1px solid @color-primary-d;
      }
      &::after {
        font-family: 'fontello';
        content: '\f107';
        position: absolute;
        top: 14px;
        right: 10px;
        font-size: 15px;
        opacity: 0.7;
        .trans-dur(@c-time);
      }
      &.collapsed {
        &::after {
          .rotate(180deg);
        }
      }
    }
  }
  .open-collapse {
    .trans-dur(@c-time);
  }
  .card-body {
    padding: 12px;
    ul {
      padding-left: 0;
      list-style: none;
      li {
        a {
          display: block;
          color: @color-primary-c;
          margin-bottom: 8px;
          padding: 4px 0;
          padding-left: 4px;
          border-bottom: 1px solid @color-primary-d;
          .trans-dur(@m-time);
          &:hover {
            color: @color-primary-e;
          }
        }
      }
    }
  }
}
</style>
