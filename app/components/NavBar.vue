<template>
  <nav class="font-mono">
    <ul class="flex space-x-4">
      <li class="link">
        <NuxtLink to="/">Main</NuxtLink>
      </li>
      <li class="link">
        <NuxtLink to="/about">About</NuxtLink>
      </li>
    </ul>
  </nav>
</template>

<style scoped>
.link {
  @apply hover:text-orange-700 p-1 hover:bg-gray-200;
}
</style>
