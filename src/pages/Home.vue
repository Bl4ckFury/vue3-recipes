<script setup>
import AppButton from "@/components/buttons/AppButton.vue";
import AppLayout from "@/layouts/AppLayout.vue";
import { RecipeService } from "@/services";
import { onMounted, ref } from "vue";

const recipes = ref();

const fetchRecipes = async () => {
  try {
    recipes.value = await RecipeService.getRecipesByLetter();
  } catch {}
};

onMounted(fetchRecipes);
</script>

<template>
  <AppLayout>
    <template #title>Рецепты</template>
    <template #controls>
      <AppButton text="Добавить рецепт" />
    </template>
    <template #inner>{{ recipes }}</template>
  </AppLayout>
</template>
