<template>
  <div class="app">
    <p>{{ jobs[1].title }} {{ jobs[1].location }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import Job from "./assets/types/Job";

export default defineComponent({
  name: "App",
  components: {},

  setup() {
    const jobs = ref<Job[]>([
      { title: "farm worker", location: "Swindon", salary: "30000", id: "1" },
      { title: "farm worker", location: "Dudley", salary: "30000", id: "2" },
      { title: "farm worker", location: "Dudley", salary: "30000", id: "3" },
      { title: "farm worker", location: "Dudley", salary: "30000", id: "4" },
      { title: "farm worker", location: "Dudley", salary: "30000", id: "5" },
    ]);
    return { jobs };
  },
});
</script>

<style></style>
