<script setup lang="ts">
import { ElScrollbar } from "element-plus";
import NewExercise from "./components/NewExercise.vue";
import ListExercises from "./components/ListExercises.vue";
</script>

<template>
  <div class="p-4">
    <ElScrollbar height="100vh" view-class="flex flex-col gap-8" noresize>
      <NewExercise />

      <ListExercises />
    </ElScrollbar>
  </div>
</template>
