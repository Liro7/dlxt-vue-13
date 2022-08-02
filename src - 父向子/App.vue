<template>
  <div>
    <product :num="n" :s="str" :flag="flag" :obj="obj"></product>
  </div>
</template>

<script>
import product from "./components/myprojuct.vue";
export default {
  components: {
    product,
  },
  data() {
    return {
      n: 10,
      str: "hello",
      flag: false,
      obj: { name: "zs" },
    };
  },
};
</script>

<style scoped>
</style>