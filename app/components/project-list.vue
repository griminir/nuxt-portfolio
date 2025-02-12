<template>
  <div>Projects</div>

  <section v-if="pending">Loading...</section>
  <section v-else-if="error"> error getting stuff</section>
  <section v-else>
    <ul>
      <li v-for="repo in data" :key="repo.id">
        <a :href="repo.html_url">{{ repo.name }}</a>
      </li>
    </ul>
  </section>
</template>

<script setup>
const { error, data, pending } = await useFetch(
  'https://api.github.com/users/griminir/repos'
);
</script>
