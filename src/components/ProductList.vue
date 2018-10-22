<template>
  <div class="product-list">
    <b-row>
      <Product
        v-for="product in products"
        v-bind:key="product.name"
        v-bind:product="product"
      />
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
        products: [
          { name:"Samsung Galaxy S9", stock: 8, price: "$707.99" },
          { name:"LG V35 ThinQ 64GB", stock: 12, price: "$649.99" },
           { name:"Xiaomi Mi Mix 2S", stock: 4, price: "$447.90" }
        ]
      }
    }
  }
</script>

<style scoped>
  .product-list {
    margin-top: 25px;
  }
</style>
