<template>
  <div id="app">
    <nav-bar></nav-bar>
    <el-row :gutter="20">
      <el-col :span="16">
        <h1>Product List</h1>
        <product-list></product-list>
      </el-col>
      <el-col :span="8">
        <h1>Shopping Cart</h1>
        <shopping-cart></shopping-cart>
        <p><b>Total Cost: {{ totalCost | currency }}</b></p>
      </el-col>
    </el-row>
    
  </div>
</template>
<script>
import {Store} from './store/Store'
export default {
  name: 'app',
  computed: {
    totalCost(){
      return Store.totalCost
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
