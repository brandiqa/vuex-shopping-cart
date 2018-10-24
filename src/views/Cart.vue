<template>
  <div class="cart">
    <h2>My Shopping Cart</h2>
    <ShoppingCart />
  </div>
</template>

<script>
 import ShoppingCart from '@/components/ShoppingCart.vue'

  export default {
    name: 'Cart',
    components: {
      ShoppingCart
    }
  }
</script>
