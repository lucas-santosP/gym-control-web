<script setup lang="ts">
import { ElInput, ElInputNumber, ElSelect } from "element-plus";
import { ref } from "vue";

const form = ref({
  exercise: "",
  repetitions: 1,
  series: 1,
  technique: "",
});
</script>

<template>
  <section>
    <h2>New exercise</h2>

    <form action="" class="flex flex-col gap-4">
      <div class="flex flex-col gap-1 flex-1">
        <label for="Exercise">Exercise*</label>
        <ElInput id="Exercise" v-model="form.exercise" required />
      </div>

      <div class="flex flex-col sm:flex-row gap-6">
        <div class="flex flex-col gap-1 flex-1">
          <label for="Technique">Technique</label>
          <ElSelect id="Technique" v-model="form.technique">
            <ElOption label="Select..." value="" disabled />
            <ElOption label="Drop 7" value="drop7" />
            <ElOption label="FST-7" value="fst7" />
            <ElOption label="GVT" value="gvt" />
          </ElSelect>
        </div>

        <div class="flex gap-6">
          <div class="flex flex-col gap-1">
            <label for="Repetitions">Repetitions*</label>
            <ElInputNumber id="Repetitions" :min="1" v-model="form.repetitions" required />
          </div>

          <div class="flex flex-col gap-1">
            <label for="Series">Series*</label>
            <ElInputNumber id="Series" :min="1" v-model="form.series" required />
          </div>
        </div>
      </div>

      <ElButton native-type="submit">Create</ElButton>
    </form>
  </section>
</template>
