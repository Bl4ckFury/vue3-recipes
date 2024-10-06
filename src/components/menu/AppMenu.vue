<script setup></script>

<template>
  <div class="menu">
    <div class="logo">
      <img src="../../assets/image/logo.png" alt="logo-img" class="logo-img" />
    </div>
    <el-menu class="el-menu-vertical-demo">
      <el-menu-item index="1">
        <el-icon :size="30"><Food /></el-icon>
      </el-menu-item>
      <el-menu-item index="2">
        <el-icon :size="30"><Dish /></el-icon>
      </el-menu-item>
      <el-menu-item index="3">
        <el-icon :size="30"><Dish /></el-icon>
      </el-menu-item>
      <el-menu-item index="4">
        <el-icon :size="30"><Dish /></el-icon>
      </el-menu-item>
      <el-menu-item index="5">
        <el-icon :size="30"><Dish /></el-icon>
      </el-menu-item>
    </el-menu>
  </div>
</template>

<style lang="scss" scoped>
@import "../../assets/styles/main.scss";

.menu {
  height: 100vh;
  border: 1px solid $gray;
  .logo {
    .logo-img {
      margin: 10px 0;
    }
  }
}
</style>
