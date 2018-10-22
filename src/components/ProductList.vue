<template>
  <div class="product-list">
    <b-row>
      <Product v-bind:product="product"/>
    </b-row>
  </div>
</template>

<script>
  import Product from './Product.vue'

  export default {
    name: 'ProductList',
    components: {
      Product
    },
    data() {
      return {
        product: {
          name:"Samsung Galaxy S9",
          stock: 16,
          price: "$707.99"
        }
      }
    }
  }
</script>

<style scoped>
  .product-list {
    margin-top: 25px;
  }
</style>
