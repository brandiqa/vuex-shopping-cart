<template>
  <div class="products">
    <h2>Top Smartphones</h2>
    <ProductList />
  </div>
</template>

<script>
// @ is an alias to /src
import ProductList from '@/components/ProductList.vue'

export default {
  name: 'home',
  components: {
    ProductList
  }
}
</script>
