<template>
  <div class="container mx-auto max-w-2xl">
    <header class="flex justify-between items-center mt-5">
      <div>
        <NuxtLink
          to="/"
          class="text-2xl font-bold p-2 hover:bg-gray-200 hover:text-orange-700"
          >Viktor E. Degray</NuxtLink
        >
      </div>
      <NavBar />
    </header>
    <main>
      <slot />
    </main>
  </div>
</template>
