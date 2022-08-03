<template>
  <div>
    <button @click="comname = 'UserName'">账号密码填写</button>
    <button @click="comname = 'UserInfo'">个人信息填写</button>
    <!-- 显示组件 -->
    <div style="border: 1px solid #333">
      <component :is="comname"></component>
    </div>
  </div>
</template>

<script>
import UserName from "@/components/UserName.vue";
import UserInfo from "@/components/UserInfo.vue";
export default {
  components: { UserName, UserInfo },
  data() {
    return {
      comname: "UserName", //存储组件名
    };
  },
};
</script>

<style scoped>
</style>