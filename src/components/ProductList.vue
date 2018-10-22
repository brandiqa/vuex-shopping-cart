<template>
  <div class="product-list">
    <b-row align-h="start" v-for="(products, index) in groupedProducts" :key="index">
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
  import _ from 'lodash';

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
          { name:"Xiaomi Mi Mix 2S", stock: 4, price: "$447.90" },
          { name:"Samsung Galaxy S8+", stock: 8, price: "$655.99" },
          { name:"IPhone XS Max", stock: 12, price: "$1499.99" },
          { name:"Google Pixel 2", stock: 4, price: "$899.90" },
          { name:"Redmi S2", stock: 12, price: "$160.99" },
        ]
      }
    },
    computed: {
      groupedProducts() {
        return _.chunk(this.products, 4)
      }
    }
  }
</script>

<style scoped>
  .product-list {
    margin-top: 25px;
  }
  .row {
    margin-bottom: 25px;
  }
</style>
