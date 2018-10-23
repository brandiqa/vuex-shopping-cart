<template>
  <div class="shopping-cart">
    <b-table striped hover head-variant="dark" :items="items" :fields="fields">
      <template slot="action" slot-scope="data">
        <b-button v-if="data.item.price != 'TOTAL'" size="sm" @click.stop variant="outline-danger">Deduct</b-button>
      </template>
    </b-table>
    <b-button variant="outline-success" class="btn-checkout">Express Checkout</b-button>
  </div>
</template>

<script>
  const items = [
    { product: 'Pocophone FI', quantity: 2, price: "$200", cost: "$400" },
    { product: 'Samsung S9', quantity: 1, price: "$900", cost: "$900" },
    { price: "TOTAL:", cost: "$1,300", _rowVariant: 'warning'}
  ]
  const fields = ['product', 'quantity', 'price','cost', 'action']

  export default {
    data () {
      return {
        fields, items
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
    color: green;
  }
  .btn-checkout {
    float:right;
  }
</style>
