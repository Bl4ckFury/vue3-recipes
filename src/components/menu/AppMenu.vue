<script setup>
import { ROUTES_PATHS } from "@/constants";
import { onMounted } from "vue";
import { useRouter, useRoute } from "vue-router";

const router = useRouter();
const route = useRoute();

const isPathActive = (path) => {
  return route.path === path;
};

onMounted(isPathActive);
</script>

<template>
  <div class="menu">
    <div class="logo">
      <img src="../../assets/image/logo.png" alt="logo-img" class="logo-img" />
    </div>
    <el-menu :router="true" class="el-menu-vertical-demo">
      <el-menu-item
        :index="ROUTES_PATHS.HOME"
        :class="['item', isPathActive(ROUTES_PATHS.HOME) && 'active']"
      >
        <el-icon :size="30"><Food /></el-icon>
      </el-menu-item>
      <el-menu-item
        :index="ROUTES_PATHS.CATEGORIES"
        :class="['item', isPathActive(ROUTES_PATHS.CATEGORIES) && 'active']"
      >
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
  .item {
    color: $violet;
    &.active {
      color: $pink;
    }
  }
}
</style>
