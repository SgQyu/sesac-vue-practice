<template>
  <h2>Component 1</h2>
  <CompLevel2 />
</template>

<script>
import CompLevel2 from "./CompLevel2";

export default {
  name: "CompLevel1",
  components: {
    CompLevel2,
  },
};
</script>

<style></style>
