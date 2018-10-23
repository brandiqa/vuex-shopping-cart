<template>
  <div class="orders">
    <h2>My Orders</h2>
    <OrderList />
  </div>
</template>

<script>
  import OrderList from '../components/OrderList.vue'

  export default {
    components: {
      OrderList
    }
  }
</script>