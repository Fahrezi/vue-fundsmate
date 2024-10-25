<script setup lang="ts">
defineProps<{
  title: string
  description: string
  img: string
}>()
</script>

<template>
  <div class="benefit-card">
    <img :src="img" alt="benefit-icon" height="232" width="232" />
    <h3>{{ title }}</h3>
    <p>{{ description }}</p>
  </div>
</template>

<style>
.benefit-card {
  @apply flex flex-col items-center justify-center px-4 md:px-8 py-8 md:py-16 shadow-lg rounded-xl gap-y-4 bg-white;
}

.benefit-card img {
  @apply w-32 md:w-48;
}

.benefit-card h3 {
  @apply font-semibold text-lg text-center md:text-xl lg:text-2xl text-slate-700;
}

.benefit-card p {
  @apply text-slate-500 text-center text-base lg:text-lg;
}
</style>
