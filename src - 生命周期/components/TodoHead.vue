<template>
  <div class="todo-head">
    <h1>todos</h1>
    <input type="checkbox" v-model="isAll" />
    <input type="text" v-model="name" @keyup.enter="addFn" />
  </div>
</template>

<script>
export default {
  props: ["list"],
  data() {
    return {
      name: "",
    };
  },
  methods: {
    computed: {
      isAll: {
        set(checked) {
          // 影响数组里每个小选框绑定的ischeck属性
          this.list.forEach((item) => {
            item.ischeck = checked;
          });
        },
        get() {},
      },
    },
    addFn() {
      // 非空判断
      if (this.name.trim().length === 0) {
        alert("任务内容不能为空");
        return;
      }
      // 子传父
      this.$emit("create", this.name);
    },
  },
};
</script>

<style scoped>
</style>