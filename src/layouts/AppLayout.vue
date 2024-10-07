<script setup>
import AppMenu from "@/components/menu/AppMenu.vue";
</script>

<template>
  <div class="root">
    <div class="menu-inner">
      <AppMenu />
    </div>
    <main class="main">
      <header class="header">
        <div class="title">
          <slot name="title"></slot>
        </div>
        <div class="controls">
          <slot name="controls"></slot>
        </div>
      </header>
      <div class="inner">
        <slot name="inner"></slot>
      </div>
    </main>
  </div>
</template>

<style lang="scss" scoped>
@import "../assets/styles/main.scss";

.root {
  display: flex;
  .menu-inner {
    width: 70px;
  }
  .main {
    flex: 1;
    padding: 15px;
    .header {
      display: flex;
      margin: 10px 0;
      align-items: center;
      justify-content: space-between;
      .title {
        color: $violet;
        font-size: 30px;
        font-weight: 700;
      }
    }
  }
}
</style>
