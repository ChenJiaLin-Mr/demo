<template>
  <div id="app">
    <van-tabbar >
      <van-tabbar-item icon="home-o" @click="funShow">标签</van-tabbar-item>
    </van-tabbar>
    <van-action-sheet
      v-model="actionSheet"
      :actions="actions"
      close-on-click-action
    />
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      actionSheet:false,
      actions: [{ name: "选项一" }, { name: "选项二" }, { name: "选项三" }],
    };
  },
  methods: {
    // 在正式环境， 这个事件有小概率会失效， 导致弹窗不能展示出来，目前已知手机型号有小米，苹果13
    funShow() {
      this.actionSheet = true;
    },
  },
};
</script>

<style></style>
