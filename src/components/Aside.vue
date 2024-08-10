<template>
  <el-menu
    default-active="2"
    class="aside-container"
    @open="handleOpen"
    @close="handleClose"
  >
    <p class="logo-lg">彩妍陪診</p>
    <TreeMenu :menuData="menuData" :index="1" />
  </el-menu>
</template>

<script setup>
import TreeMenu from "./TreeMenu.vue";
import { useRouter } from "vue-router";
import { reactive } from "vue";
const router = useRouter();

const menuData = reactive(router.options.routes[0].children);

const handleOpen = () => {};
const handleClose = () => {};
</script>

<style scoped lang="scss">
.aside-container {
  background: rgba(#000, 0.4);
  height: 100%;
  .logo-lg {
    font-size: 20px;
    text-align: center;
    height: 50px;
    line-height: 50px;
    color: #fff;
  }
}
</style>
