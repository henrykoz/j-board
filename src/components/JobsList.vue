<template>
  <div class="job-list">
    <ul>
      <li v-for="job in jobs" :key="job.id">
        <h2>{{ job.title }} in {{ job.location }}</h2>
        <div class="salary">
          <p>{{ job.salary }} pounds</p>
        </div>
        <div class="description">
          <p>
            Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et fugiat
            quaerat, sequi est architecto doloremque incidunt deleniti quidem
            debitis in pariatur accusamus veniam dicta fuga! Quae inventore
            dolores et repellendus!
          </p>
        </div>
      </li>
    </ul>
  </div>
</template>

ts
<script lang="ts">
import { defineComponent, PropType } from "vue";
import Job from "@/assets/types/Job";

export default defineComponent({
  props: {
    jobs: {
      required: true,
      type: Array as PropType<Job[]>,
    },
  },
});
</script>

<style scoped>
.job-list {
  max-width: 960px;
  margin: 40px auto;
}
.job-list li {
  list-style-type: none;
  background: white;
  padding: 16px;
  margin: 16px 0;
  border-radius: 4px;
}
.job-list h2 {
  margin: 0 0 10px;
  text-transform: capitalize;
}
.salary {
  display: flex;
}
.salary img {
  width: 30px;
}
.salary p {
  color: green;
  font-weight: bold;
}
</style>
