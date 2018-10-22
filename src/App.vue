<template>
  <div id="app">
    <b-jumbotron  bg-variant="info" text-variant="white">
      <template slot="header">
        Vuex Shopping Cart
      </template>
      <template slot="lead">
        Built using Bootstrap-Vue.js
      </template>
    </b-jumbotron>

    <b-container>
      <b-nav pills>
        <router-link class="nav-link" to="/" exact>Home</router-link>
        <router-link class="nav-link" to="/cart">Cart (0)</router-link>
        <router-link class="nav-link" to="/orders">Orders</router-link>
      </b-nav>
      <router-view/>
    </b-container>

  </div>
</template>

<style>
.active {
  background-color: #17A2B8 !important;
}
</style>
