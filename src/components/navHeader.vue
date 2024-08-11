<template>
  <div class="header-container">
    <div class="header-left">
      <el-icon class="icon" @click="store.commit('collapseMenu')"
        ><Fold></Fold
      ></el-icon>
    </div>
    <div class="header-right">
      <el-dropdown>
        <div class="el-dropdown-link">
          <el-avatar
            src="https://cube.elemecdn.com/0/88/03b0d39583f48206768a7534e55bcpng.png"
          />
          <p class="username">admin</p>
        </div>
        <template #dropdown>
          <el-dropdown-menu>
            <el-dropdown-item>Action 1</el-dropdown-item>
            <el-dropdown-item>Action 2</el-dropdown-item>
            <el-dropdown-item>Action 3</el-dropdown-item>
            <el-dropdown-item disabled>Action 4</el-dropdown-item>
            <el-dropdown-item divided>Action 5</el-dropdown-item>
          </el-dropdown-menu>
        </template>
      </el-dropdown>
    </div>
  </div>
</template>

<script setup>
import { useStore } from "vuex";
const store = useStore();
</script>

<style lang="scss" scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100%;
  background: #fff;
  padding-right: 25px;
  .header-left {
    display: flex;
    align-items: center;
    height: 100%;

    .icon {
      width: 45px;
      height: 100%;
      cursor: pointer;
      &:hover {
        background: #f5f5f5;
      }
    }
  }
  .header-right {
    .el-dropdown-link {
      display: flex;
      align-items: center;
      .username {
        margin-left: 15px;
      }
    }
  }
}
</style>
