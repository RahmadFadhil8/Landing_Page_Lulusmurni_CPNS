<template>
  <div class="flex flex-col max-w-xs bg-white rounded-2xl shadow-lg border border-gray-100 overflow-hidden transition hover:shadow-xl">
    <div class="p-6 bg-linear-to-b from-orange-100 to-white grow">
      <h2 class="text-2xl font-bold text-gray-900 mb-1">{{ product.title }}</h2>
      <p class="text-gray-600 text-sm mb-4">{{ product.description }}</p>
      <span class="text-lg font-bold text-gray-900">
        Rp{{ product.price?.toLocaleString() || '0' }}
      </span>
    </div>
    <div class="p-6 pt-2 grow">
      <ul class="space-y-3 mb-6">
        <li v-for="benefit in product.benefit" :key="benefit" class="flex items-center gap-3 text-gray-700">
          <img src="~/assets/icon/green-check.svg" alt="">
          <p class="text-sm">{{ benefit }}</p>
        </li>
      </ul>

    </div>
    <div class="p-6">
      <NuxtLink :to="product.link">
        <button class="w-full border-2 border-blue-400 text-blue-500 font-semibold py-3 rounded-xl hover:bg-blue-50 transition duration-300 ">
          Daftar Sekarang
        </button>
      </NuxtLink>
    </div>
  </div>
</template>

<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})
</script>