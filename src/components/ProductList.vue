<template>
  <div class="product-list">
    <b-row>
      <b-col>
        <b-card class="text-centers"  title="Samsung Galaxy S9">
          <ul>
            <li><span class="bold">Stock : </span>25</li>
            <li><span class="bold">Price : </span>$1,000</li>
          </ul>
          <b-button variant="info">Add to Cart</b-button>
        </b-card>
      </b-col>
      <b-col>
        <b-card class="text-centers"  title="Xiaomi Explorer">
          <ul>
            <li><span class="bold">Stock : </span>25</li>
            <li><span class="bold">Price : </span>$1,000</li>
          </ul>
          <b-button variant="info">Add to Cart</b-button>
        </b-card>
      </b-col>
      <b-col>
        <b-card class="text-centers"  title="Oppo Find X">
          <ul>
            <li><span class="bold">Stock : </span>25</li>
            <li><span class="bold">Price : </span>$1,000</li>
          </ul>
          <b-button variant="info">Add to Cart</b-button>
        </b-card>
      </b-col>
    </b-row>

  </div>
</template>

<script>
export default {
  name: 'ProductList',
  props: { }
}
</script>

<style scoped>
.product-list {
  margin-top: 25px;
}
button {
  float: right;
}
.bold {
  font-weight: bold;
}
</style>
