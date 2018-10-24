<template>
  <div class="order-list">
    <b-table striped hover head-variant="dark" :fields="fields" :items="items">
      <template slot="orderNo" slot-scope="data">
        #00{{ data.index + 1}}
      </template>
    </b-table>
  </div>
</template>

<script>
  const fields = ["orderNo", "products", "totalCost"]
  const items = [
    { products: "2x Pocophone @ $350, 1x Samsung S9 @ $700", totalCost: "$1,300" },
  ]

  export default {
    data () {
      return {
        fields, items
      }
    }
  }
</script>