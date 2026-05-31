<template>
  <nav 
    :class="[
      'fixed w-full top-0 z-50 px-24 py-4 flex justify-between items-center transition-all duration-300',
      isScrolled ? 'bg-white shadow-md' : 'bg-transparent'
    ]"
  >
    <NuxtLink to="/">
      <img src="~/assets/images/lulusMurniASN .png" alt="logo" class="h-11 w-auto">
    </NuxtLink> 
    <ul class="flex gap-10">
      <li><NuxtLink to="/" class="text-sm">Apa itu ASN atau CPNS?</NuxtLink></li>
      <li><NuxtLink to="/" class="text-sm">Portofolio</NuxtLink></li>
      <li><NuxtLink to="/" class="text-sm">Benefit</NuxtLink></li>
      <li><NuxtLink to="/" class="text-sm">Pilihan Paket</NuxtLink></li>
      <li><NuxtLink to="/" class="text-sm">Testimoni</NuxtLink></li>
      <li><NuxtLink to="/" class="text-sm">FAQ</NuxtLink></li>
    </ul>
  </nav>
</template>

<script setup>
// Pastikan baris ini berada tepat di dalam <script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50;
};

// Hook ini harus berada di level atas, bukan di dalam fungsi lain
onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>