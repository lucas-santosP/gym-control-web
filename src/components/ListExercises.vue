<script setup lang="ts">
import { ref } from "vue";
import { ElTable } from "element-plus";

const exercises = ref([
  {
    exercise: "Agachamento livre",
    repetitions: 2,
    series: 3,
    technique: "GVT",
  },
]);
</script>

<template>
  <section>
    <h2>List Exercise</h2>

    <ElTable style="width: 100%" :data="exercises">
      <ElTableColumn type="expand">
        <template #default="props">
          <div>
            <h3>Family</h3>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. In, perferendis.</p>
          </div>
        </template>
      </ElTableColumn>

      <ElTableColumn prop="exercise" label="Exercise" width="180" />
      <ElTableColumn prop="repetitions" label="Reps" width="180" />
      <ElTableColumn prop="series" label="Series" />
      <ElTableColumn prop="technique" label="Technique" />
    </ElTable>
  </section>
</template>
