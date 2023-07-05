<template>
  <h2>Hello Reusability</h2>
  <hr />
  <FeeStatus />
  <ProductStatus />
  <SavingStatus />
</template>

<script>
import FeeStatus from "../Mixin/FeeStatus";
import ProductStatus from "../Mixin/ProductStatus";
import SavingStatus from "../Mixin/SavingStatus";

export default {
  name: "TestComponent",
  components: {
    FeeStatus,
    ProductStatus,
    SavingStatus,
  },
};
</script>

<style></style>
