<template>
  <div>
    MyProduct
    <Button @click="subFn">传递数据</Button>
  </div>
</template>

<script>
// 导入事件总线
import eventBus from "../EventBus/index";
export default {
  data() {
    return {
      num: 89,
    };
  },
  methods: {
    subFn() {
      // 事件总线 触发自定义事件
      eventBus.$emit("send", this.num);
    },
  },
};
</script>

<style scoped>
</style>