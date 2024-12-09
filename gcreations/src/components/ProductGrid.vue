<template>
  <section class="product-grid">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :product="product"
    />
  </section>
</template>

<script>
import ProductCard from "./ProductCard.vue";

export default {
  components: { ProductCard },
  data() {
    return {
      products: [
        { id: 1, name: "Handmade Necklace", image: "https://via.placeholder.com/200" },
        { id: 2, name: "Artisanal Bracelet", image: "https://via.placeholder.com/200" },
        { id: 3, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 4, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 5, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 6, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 7, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 8, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 9, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
        { id: 10, name: "Custom Earrings", image: "https://via.placeholder.com/200" },
      ],
    };
  },
};
</script>

<style>
.product-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 20px;
  padding: 20px 40px;
}
</style>
