<template>
  <p>Take a look at some of my GitHub projects!</p>
  <br />
  <section v-if="pending">Loading...</section>
  <section v-else-if="error">error getting stuff</section>
  <section v-else>
    <ul class="grid grid-cols-1 gap-4">
      <li v-for="repo in dataToDisplay" :key="repo.id" class="link">
        <a :href="repo.html_url" target="_blank">
          <div class="font-semibold">{{ repo.name }}</div>
        </a>
      </li>
    </ul>
  </section>
</template>

<script setup>
const { error, data, pending } = await useFetch(
  'https://api.github.com/users/griminir/repos'
);

const dataToDisplay = computed(() =>
  data.value.filter((repo) => repo.name !== 'griminir')
);
</script>

<style scoped>
.link {
  @apply border border-gray-200 rounded-sm hover:bg-gray-100 font-mono items-center p-2 hover:text-orange-700;
}
</style>
