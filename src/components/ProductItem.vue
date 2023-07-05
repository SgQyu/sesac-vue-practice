<template>
  <li>
    <p class="title">{{ product.name }}</p>
    <p class="image">
      <img
        :src="`http://placehold.it/320x100.png/${product.id}`"
        :alt="product.name"
      />
    </p>
    <p class="price">{{ product.price }}</p>
  </li>
</template>

<script>
export default {
  name: "product-item",
  props: {
    product: {
      type: Object,
    },
  },
};
</script>

<style scoped>
li {
  border: 2px solid salmon;
  margin-bottom: 0.5rem;
}
.title {
  font-size: 24px;
  color: #2c82c9;
  font-weight: bold;
}
</style>
