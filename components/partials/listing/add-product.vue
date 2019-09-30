<template>
  <div class="add-to-card">
    <div class="quantity-toggle">
      <button class="click" @click="decrement()">
        &mdash;
      </button>
      <b-input type="number" class="quant-input" :value="quantity" />
      <button class="click" @click="increment()">
        &#xff0b;
      </button>
    </div>
    <b-button type="submit" class="a-dark">
      add to card
    </b-button>
  </div>
</template>

<script>
export default {
  name: 'AddProduct',
  data() {
    return {
      quantity: 1
    }
  },
  methods: {
    increment() {
      this.quantity++
    },
    decrement() {
      if (this.quantity === 0) {
        alert('Negative quantity not allowed')
      } else {
        this.quantity--
      }
    }
  }
}
</script>

<style lang="less" scoped>
.add-to-card {
  display: flex;
  align-items: center;
  justify-content: center;
}
.quantity-toggle {
  display: flex;
  align-items: center;
  justify-content: center;
  max-width: 120px;
  border: 1px solid @color-primary-i;
  margin-right: 50px;
}
.form-control:disabled,
.form-control {
  background-color: transparent;
  border: none;
  text-align: center;
  padding: 0;
  &:focus {
    box-shadow: 0 0 0 0.2rem rgba(255, 255, 255, 0.25);
  }
}
.click {
  border: none;
  background-color: transparent;
  padding: 9px;
  .trans-dur(@m-time);
  &:hover {
    background-color: @color-primary-h;
  }
  &:focus {
    outline: none;
  }
}
.a-dark {
  padding-top: 10px;
  padding-bottom: 10px;
}
</style>
