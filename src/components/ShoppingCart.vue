<template>
  <div class="shopping-cart">
    <b-table striped hover head-variant="dark" :items="items"></b-table>
  </div>
</template>

<script>
  const items = [
    { product: 'Pocophone FI', quantity: 2, price: "$200", cost: "$400" },
    { product: 'Samsung S9', quantity: 2, price: "$200", cost: "$900" },
    { price: "TOTAL:", cost: "$1300"}
  ]

  export default {
    name: 'ShoppingCart',
    data () {
      return {
        items: items
      }
    }
  }
</script>

<style>
  table {
    margin-top: 24px;
  }
  .shopping-cart tr:last-child {
    font-weight: bold !important;
    color: cornflowerblue;
  }
</style>
