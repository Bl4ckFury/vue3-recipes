<script setup>
const props = defineProps({
  text: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <el-button type="primary" class="btn">{{ text }}</el-button>
</template>

<style lang="scss" scoped>
@import "../../assets/styles/main.scss";

.btn {
  height: 50px;
  width: 200px;
  color: $white;
  cursor: pointer;
  font-size: 18px;
  border-radius: 5px;
  background-color: $violet;
  transition: all 0.2s ease-in-out;
  &:hover {
    color: $violet;
    background-color: $white;
    border: 2px solid $violet;
  }
}
</style>
