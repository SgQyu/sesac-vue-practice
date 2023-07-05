<template>
  <hr />
  <h3>{{ fullname }}</h3>
  <button @click="sendParent">child click</button>
</template>

<script>
import { computed } from "vue";

export default {
  name: "childComponents",
  // props: ["firstname", "lastname"],
  props: {
    firstname: {
      type: String,
      default: "",
    },
    lastname: {
      type: String,
      default: "",
    },
  },
  setup(props, context) {
    const fullname = computed(() => {
      return `${props.firstname} ${props.lastname}`;
    });
    function sendParent() {
      context.emit("sendParent");
      console.log(props);
      console.log(context);
    }

    return {
      fullname,
      sendParent,
    };
  },
};
</script>

<style></style>
