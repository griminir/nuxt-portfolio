<template>
  <div>
    <h2 class="text-2xl font-semibold mb-10">Projects</h2>
    <ProjectList />
  </div>
</template>

<script setup>
import ProjectList from '~/components/project-list.vue';

useHead({
  title: 'Projects Page',
  description: 'Projects page for Viktor E. Degray',
});
</script>
