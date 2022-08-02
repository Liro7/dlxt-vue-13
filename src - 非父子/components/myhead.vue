<template>
  <div>
    {{ n }}
  </div>
</template>

<script>
// 引入事件总线
// 接收方-----$on监听事件  定义自定义事件
import eventBus from "../EventBus/index";
export default {
  data() {
    return {
      n: 0,
    };
  },
  // 组件创建完毕，监听send事件
  created() {
    eventBus.$on("send", (v) => {
      alert(v);
      this.n = v;
    });
  },
};
</script>

<style scoped>
</style>