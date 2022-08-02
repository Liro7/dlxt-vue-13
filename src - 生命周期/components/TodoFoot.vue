<template>
  <div class="todo-foot">
    <div>剩余{{ farr.length }}</div>
    <ul @click="fn">
      <li @click="isSel = 'all'" :class="{ active: isSel === 'all' }">全部</li>
      <li @click="isSel = 'yes'" :class="{ active: isSel === 'yes' }">
        已完成
      </li>
      <li @click="isSel = 'no'" :class="{ active: isSel === 'no' }">未完成</li>
    </ul>
    <button @click="clearFn">清楚已完成</button>
  </div>
</template>

<script>
export default {
  props: ["farr"],
  data() {
    return {
      // 1.变量isSel
      isSel: "all", //all指的是全部  yes是已完成  no是未完成
    };
  },
  methods: {
    clearFn() {
      // 点击清空已完成
      // 触发父组件中的事件
      this.$emit("clearEvent");
    },
    fn() {
      // 点击全部，已完成，未完成
      // 子传父  把isSel的值传给App.vue
      this.$emit("changeType", this.isSel);
    },
  },
};
</script>

<style scoped>
.todo-foot {
  display: flex;
  height: 50px;
  border-top: 1px solid red;
  align-items: center;
  justify-content: space-between;
}
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  width: 200px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 5px;
  height: 50px;
}
ul .active {
  border: 1px solid red;
}
</style>