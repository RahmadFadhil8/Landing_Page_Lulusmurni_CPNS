<template>
  <div class="max-w-sm rounded-2xl overflow-hidden shadow-lg bg-white border border-gray-100 transition hover:shadow-xl">
    <img class="w-full h-48 object-cover" :src="image" :alt="title" />
    
    <div class="p-6">
      <h2 class="text-xl font-bold text-gray-900 mb-3">{{ title }}</h2>
      <p class="text-gray-600 text-sm leading-relaxed mb-6">
        {{ description }}
      </p>
      <NuxtLink to="#" class="text-blue-600 font-semibold hover:underline">
        {{ linkText }} &rarr;
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
defineProps({
  image: String,
  title: String,
  description: String,
  linkText: {
    type: String,
    default: 'Learn More'
  }
})
</script>