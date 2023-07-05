<template>
  <div>Parent Comp</div>
  <input v-model="nickname" ref="inputRef" />
  <button @click="consoleRef">console ref</button>
  <hr />
  <ChildComp v-if="showChild" ref="childRef" />
  <button @click="showChild = false">unmount child</button>
</template>

<script>
import ChildComp from "./ChildComp";

export default {
  name: "ParentComp",
  components: {
    ChildComp,
  },
  data() {
    return {
      showChild: true,
      nickname: "",
    };
  },
  methods: {
    consoleRef() {
      console.log(this.$refs.inputRef, "input ref");
      console.log(this.$refs.childRef, "childComp ref");
      this.$refs.childRef.sayHello();
    },
  },
};
</script>

<style></style>
