<template>
  <div id="app">
    <b-jumbotron  bg-variant="info" text-variant="white">
      <template slot="header">
        Vue Shopping Cart
      </template>
      <template slot="lead">
        Powered by Vuex
      </template>
    </b-jumbotron>

    <b-container>
      <b-nav pills>
        <router-link class="nav-link" to="/" exact>Home</router-link>
        <router-link class="nav-link" to="/orders">Orders</router-link>
      </b-nav>
      <router-view/>
    </b-container>

  </div>
</template>

<style>

</style>
