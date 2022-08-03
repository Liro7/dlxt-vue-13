<template>
  <div>
    <ComNameHaha></ComNameHaha>
  </div>
</template>

<script>
import Com from "./components/Com.vue";
export default {
  // 对象里的key是变量的话 []属性名表达式
  components: { Tick, [Com.name]: Com },
};
</script>

<style scoped>
</style>