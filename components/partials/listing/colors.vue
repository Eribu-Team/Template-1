<template>
  <div class="listing-colors l-colors">
    <h2 class="sidebar-title text-t-capitalize">
      Color
    </h2>
    <div>
      <ul>
        <li>
          <b-form-checkbox
            id="checkbox-1"
            name="checkbox1"
            value="accepted"
            class="single-color bg-amber"
          >
            Amber
          </b-form-checkbox>
        </li>
        <li>
          <b-form-checkbox
            id="checkbox-2"
            name="checkbox2"
            value="accepted"
            class="single-color bg-black"
          >
            Black
          </b-form-checkbox>
        </li>
        <li>
          <b-form-checkbox
            id="checkbox-3"
            name="checkbox3"
            value="accepted"
            class="single-color bg-red"
          >
            Red
          </b-form-checkbox>
        </li>
        <li>
          <b-form-checkbox
            id="checkbox-4"
            name="checkbox4"
            value="accepted"
            class="single-color bg-antique"
          >
            Antique
          </b-form-checkbox>
        </li>
        <li>
          <b-form-checkbox
            id="checkbox-5"
            name="checkbox5"
            value="accepted"
            class="single-color bg-green"
          >
            Green
          </b-form-checkbox>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Colors'
}
</script>

<style lang="less" scoped>
ul {
  padding-left: 0;
  list-style-type: none;
  li {
    display: flex;
    align-items: center;
    justify-content: center;
    margin: 0 5px 3px;
    &:first-of-type {
      margin-left: 0;
    }
    &:last-of-type {
      margin-right: 0;
    }
    .single-color {
      font-weight: 400;
      color: @color-primary-c;
      &::after {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        right: 0;
        content: '';
        width: 15px;
        height: 15px;
        border-radius: 50%;
        pointer-events: none;
      }
      &:hover {
        color: @color-black;
      }
      &.bg-amber {
        &::after {
          background-color: @bg-amber;
        }
      }
      &.bg-black {
        &::after {
          background-color: @bg-black;
        }
      }
      &.bg-red {
        &::after {
          background-color: @bg-red;
        }
      }
      &.bg-antique {
        &::after {
          background-color: @bg-antique;
        }
      }
      &.bg-green {
        &::after {
          background-color: @bg-green;
        }
      }
    }
    span {
      display: block;
    }
  }
}
</style>
