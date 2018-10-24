<template>
  <b-col class="product" cols="3">
    <b-card class="text-centers" :title="product.name">
      <ul>
        <li><span>Specs : </span>{{product.specs}} </li>
        <li><span>Price : </span>{{product.price}} </li>
        <li><span>Stock : </span>{{product.stock}}</li>
      </ul>
      <b-button variant="outline-success">Add to Cart</b-button>
    </b-card>
  </b-col>
</template>

<script>
  export default {
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
  .card-title {
    font-size: 1.2rem;
  }
</style>
