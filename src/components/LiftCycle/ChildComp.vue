<template>
  <h2>Child components</h2>
  <input type="text" v-model="username" />
</template>

<script>
export default {
  name: "ChildComp",
  data() {
    return {
      username: "",
    };
  },
  methods: {
    sayHello() {
      console.log("say hello");
    },
  },
};
</script>

<style></style>
