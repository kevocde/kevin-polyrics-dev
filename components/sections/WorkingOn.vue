<template>
  <CommonResponsiveContainer class="workingon">
    <div class="workingon__title px-4 text-center font-bold mb-10">
      <h3 class="text-2xl md:text-3xl xl:text-4xl">Working On</h3>
      <p class="text-gray-500 text-sm md:text-md xl:text-lg">Projects, Contributions, Ideas and more</p>
    </div>
    <div class="workingon__projects px-4 grid gap-4 md:grid-cols-2 lg:grid-cols-3 2xl:grid-cols-4">
      <CommonCardProject v-for="project in projects" :title="project.title" :description="project.description" :coverImg="project.coverImg" :github="project.github" :website="project.website"></CommonCardProject>
    </div>
  </CommonResponsiveContainer>
</template>

<script lang="ts" setup>
  import type { ProjectDto } from '~/typos/ProjectDto';

  defineProps({
    projects: { type: Array<ProjectDto>, required: true }
  });

</script>

<style>
  .workingon {
    padding-top: 10rem;
    padding-bottom: 10rem;
  }
</style>