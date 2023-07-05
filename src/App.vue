<template>
  <div>
    <h2>Hello Composition API</h2>
    <TestComponents />
  </div>
</template>

<script>
import TestComponents from "./components/Composition/TestComponents";

export default {
  name: "App",
  components: {
    TestComponents,
  },
  data() {
    return {};
  },
};
</script>

<style></style>
