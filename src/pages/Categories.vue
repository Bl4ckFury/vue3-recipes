<script setup>
import AppButton from "@/components/buttons/AppButton.vue";
import AppLayout from "@/layouts/AppLayout.vue";
</script>

<template>
  <AppLayout>
    <template #title>Категории</template>
    <template #controls>
      <AppButton text="Добавить категорию" />
    </template>
    <template #inner></template>
  </AppLayout>
</template>
