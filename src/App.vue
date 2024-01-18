<template>
  <div class="app">
    <JobList :jobs="jobs" />
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import JobList from "./components/JobsList.vue";
import Job from "./assets/types/Job";

export default defineComponent({
  name: "App",
  components: { JobList },

  setup() {
    const jobs = ref<Job[]>([
      { title: "farm worker", location: "Swindon", salary: "30000", id: "1" },
      { title: "technican", location: "Dudley", salary: "24000", id: "2" },
      { title: "stone mason", location: "Rome", salary: "28000", id: "3" },
      { title: "engineer", location: "Birmingham", salary: "32000", id: "4" },
      {
        title: "factory worker",
        location: "Hinckley",
        salary: "16000",
        id: "5",
      },
    ]);
    return { jobs };
  },
});
</script>

<style scoped>

</style>
