<template>
  <div class="order-list">
    <b-table striped hover head-variant="dark" :items="items"></b-table>
  </div>
</template>

<script>
  const items = [
    { orderDate: "2018-10-16", products: "2x Pocophone @ $350, 1x Samsung S9 @ $700", total: "$1,300" },
  ]

  export default {
    data () {
      return {
        items: items
      }
    }
  }
</script>