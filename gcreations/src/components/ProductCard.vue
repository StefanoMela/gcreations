<template>
  <div class="product-card">
    <img :src="product.image" :alt="product.name" />
    <h3>{{ product.name }}</h3>
  </div>
</template>

<script>
export default {
  props: {
    product: Object,
  },
}
</script>

<style>
.product-card {
  background: #fff;
  padding: 15px;
  text-align: center;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s;
}

.product-card img {
  max-width: 100%;
  border-radius: 10px;
}

.product-card h3 {
  margin: 10px 0 0;
  font-size: 18px;
}

.product-card:hover {
  transform: scale(1.05);
}
</style>
