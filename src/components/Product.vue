<template>
  <div class="product">
    <b-col>
      <b-card class="text-centers" :title="product.name">
        <ul>
          <li><span class="bold">Stock : </span>{{product.stock}}</li>
          <li><span class="bold">Price : </span>{{product.price}} </li>
        </ul>
        <b-button variant="info">Add to Cart</b-button>
      </b-card>
    </b-col>
  </div>
</template>

<script>
  export default {
    name: 'Product',
    props: ['product']
  }
</script>

<style scoped>
  button {
    float: right;
  }
  .bold {
    font-weight: bold;
  }
</style>
