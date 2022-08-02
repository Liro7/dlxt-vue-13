<template>
  <div>
    <h3>案例：折叠面板</h3>
    <div>
      <div class="title">
        <h4>{{ title }}</h4>
        <span class="btn" @click="isshow = !isshow">
          {{ isshow ? "收起" : "展开" }}
        </span>
      </div>
      <div class="container" v-show="isshow">
        <p>寒雨连夜降入屋</p>
        <p>寒雨连夜降入屋</p>
        <p>寒雨连夜降入屋</p>
        <p>寒雨连夜降入屋</p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: ["title"],
  data() {
    return {
      isshow: false,
    };
  },
};
</script>
<style scoped>
</style>