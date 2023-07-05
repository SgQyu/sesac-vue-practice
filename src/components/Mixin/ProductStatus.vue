<template>
  <div>
    <h2>전체 금액: {{ totalMoney }}원</h2>
    <div>
      <button @click="addMoney(100)">100원</button>
      <button @click="addMoney(200)">200원</button>
      <button @click="addMoney(300)">300원</button>
      <button @click="addMoney(400)">400원</button>
    </div>
  </div>
</template>

<script>
import useMoney from "../../composables/useMoney";

export default {
  name: "productStatus",
  setup() {
    const { addMoney, totalMoney } = useMoney();

    return {
      addMoney,
      totalMoney,
    };
  },
};
</script>

<style></style>
