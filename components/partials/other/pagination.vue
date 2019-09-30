<template>
  <div>
    <div class="main-pagination overflow-auto">
      <b-pagination
        v-model="currentPage"
        :total-rows="rows"
        :per-page="perPage"
        first-text="<<"
        prev-text=""
        next-text=""
        last-text=">>"
        aria-controls="my-table"
      >
        <template v-slot:prev-text>
          Previous page
        </template>
        <template v-slot:next-text>
          Next page
        </template>
      </b-pagination>
    </div>

    <!-- ODKOMENTUJ PONIŻSZE, ABY ZOBACZYĆ JAK FAJNIE PAGINACJA DZIAŁA:) -->

    <!-- <b-table
      id="my-table"
      :items="items"
      :per-page="perPage"
      :current-page="currentPage"
      small
    /> -->
  </div>
</template>

<script>
export default {
  name: 'Pagination',
  data() {
    return {
      perPage: 3,
      currentPage: 1,
      items: [
        { id: 1, first_name: 'Fred', last_name: 'Flintstone' },
        { id: 2, first_name: 'Wilma', last_name: 'Flintstone' },
        { id: 3, first_name: 'Barney', last_name: 'Rubble' },
        { id: 4, first_name: 'Betty', last_name: 'Rubble' },
        { id: 5, first_name: 'Pebbles', last_name: 'Flintstone' },
        { id: 6, first_name: 'Bamm Bamm', last_name: 'Rubble' },
        { id: 7, first_name: 'The Great', last_name: 'Gazzoo' },
        { id: 8, first_name: 'Rockhead', last_name: 'Slate' },
        { id: 9, first_name: 'Pearl', last_name: 'Slaghoople' }
      ]
    }
  },
  computed: {
    rows() {
      return this.items.length
    }
  }
}
</script>

<style lang="less" scoped>
/deep/.main-pagination {
  display: flex;
  align-items: center;
  justify-content: center;
  border-top: 1px solid @color-primary-g;
  margin: 50px 0 60px;
  padding-top: 20px;
  .page-link,
  .page-item {
    &:focus,
    &:active {
      outline: none;
      box-shadow: none;
    }
  }
  .page-link {
    color: @color-primary-j;
    font-size: 12px;
    line-height: 1;
    font-weight: 600;
    letter-spacing: 1px;
    text-transform: uppercase;
    border: none;
  }
  .page-item {
    &:nth-of-type(2) {
      margin-right: auto;
    }
    &.active,
    &:hover {
      .page-link {
        background-color: transparent;
        color: @color-primary-a;
      }
    }

    &.disabled {
      cursor: not-allowed;
      &:hover {
        .page-link {
          color: @color-primary-j;
        }
      }
    }
  }
}
</style>
