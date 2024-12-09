<template>
  <div id="app">
    <Header />
    <HeroBanner />
    <ProductGrid />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import HeroBanner from './components/HeroBanner.vue'
import ProductGrid from './components/ProductGrid.vue'
import Footer from './components/Footer.vue'

export default {
  components: {
    Header,
    HeroBanner,
    ProductGrid,
    Footer,
  },
}
</script>

<style>
body {
  font-family: 'Arial', sans-serif;
  margin: 0;
  background-color: #f9f9f9;
}
</style>
