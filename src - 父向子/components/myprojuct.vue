<template>
  <div>
    子组件
    <hr />
    {{ num }}----{{ s }}---{{ flag }}
    {{ obj.name }}
  </div>
</template>

<script>
export default {
  //   props: ["num", "s", "flag", "obj"],
  props: {
    // 必须是数字类型
    num: Number,
    //必须是数字或者字符串
    s: [String, Number],
    // 布尔类型，默认为true
    flag: {
      type: Boolean,
      default: true,
    },
    // 如果是对象或者数组，默认必须是一个函数返回
    obj: {
      type: Object,
      default: function () {
        return {};
      },
    },
  },
};
</script>

<style scoped>
</style>