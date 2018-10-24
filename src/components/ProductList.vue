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
          { name:"Samsung S9+", specs: "6.2' 64GB", stock: 8, price: "$709.00" },
          { name:"Pocophone F1", specs: "6.18' 64GB", stock: 12, price: "$370" },
          { name:"Apple iPhone X", specs: "5.8' 64GB", stock: 9, price: "$1,069.00" },
          { name:"Huwaei P20 Pro", specs: "6.1' 128GB", stock: 16, price: "$728.99" },
          { name:"Huawei Mate 20 Pro", specs: "6.53' 256GB", stock: 24, price: "$975.90" },
          { name:"Redmi S2", specs: "5.99 32GB", stock: 5, price: "$160.99" },
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
