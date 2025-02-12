<template>
  <div>
    <h1>we are inside a goal</h1>
  </div>
  <div>
    <h2>Goal ID: {{ route.params.id }}</h2>
  </div>
</template>

<script setup>
const route = useRoute();
</script>