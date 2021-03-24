<template>
  <div id="app">
    <NavBar/>
    <Header/>
    <a id="WhatAreDigitalSecurities"/>
    <Article/>
    <DigitalAssets/>
    <a id="Products"/>
    <Products/>
  </div>
</template>

<!---->
<script>
import NavBar from './components/NavBar.vue'
import Header from "./components/Header";
import Article from "./components/Article";
import DigitalAssets from "@/components/DigitalAssets";
import Products from "@/components/Products";

export default {
  name: 'App',
  components: {
    Products,
    DigitalAssets,
    Article,
    Header,
    NavBar
  }
}
</script>

<!---->
<style>

  * {
    box-sizing: border-box;
  }

  #app {
    max-width: 1920px;
    margin: 0 auto;
    overflow: hidden;
  }
</style>
