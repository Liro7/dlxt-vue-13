<template>
  <div>
    <!-- 自定义事件 abcEvent  触发abcFn 就会执行函数abcFn -->
    <my-product @abcEvent="abcFn"></my-product>
  </div>
</template>

<script>
import MyProduct from "./components/MyProduct.vue";
export default {
  components: { MyProduct },
  methods: {
    abcFn(v) {
      // v就是触发自定义事件传递的参数
      console.log("触发了", v);
    },
  },
};
</script>

<style scoped>
</style>