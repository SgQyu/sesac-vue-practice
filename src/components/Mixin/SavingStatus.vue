<template>
  <div>
    <h2>합산된 총 적금 : {{ totalMoney }}원</h2>
    <button @click="addMoney(1000)">1000원</button>
    <button @click="addMoney(2000)">2000원</button>
    <button @click="addMoney(1150)">1150원</button>
    <button @click="addMoney(2200)">2200원</button>
  </div>
</template>

<script>
import useMoney from "../../composables/useMoney";

export default {
  name: "savigStatus",
  setup() {
    const { addMoney, totalMoney } = useMoney(5000);

    return {
      addMoney,
      totalMoney,
    };
  },
};
</script>

<style></style>
