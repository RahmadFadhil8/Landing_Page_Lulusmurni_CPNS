<template>
  <nav 
    :class="[
      'fixed w-full top-0 z-50 transition-all duration-300',
      isScrolled ? 'bg-white shadow-md' : 'bg-transparent',
      isMenuOpen ? 'bg-white shadow-md' : 'bg-transparent',
    ]"
  >
    <div class="flex justify-between items-center px-6 lg:px-24 py-4">
      <NuxtLink to="/">
        <img src="~/assets/images/lulusMurniASN .png" alt="logo" class="h-11 w-auto">
      </NuxtLink> 
      <ul class="hidden lg:flex gap-10">
        <li><NuxtLink to="#CPNS" class="text-sm">Apa itu CPNS?</NuxtLink></li>
        <li><NuxtLink to="#Masalah" class="text-sm">Masalah</NuxtLink></li>
        <li><NuxtLink to="#Solusi" class="text-sm">Solusi</NuxtLink></li>
        <li><NuxtLink to="#Benefit" class="text-sm">Benefit</NuxtLink></li>
        <li><NuxtLink to="#Paket" class="text-sm">Pilihan Paket</NuxtLink></li>
        <li><NuxtLink to="#FAQ" class="text-sm">FAQ</NuxtLink></li>
      </ul>
  
      <!-- Mobile Button -->
      <button
        @click="isMenuOpen = !isMenuOpen"
        class="lg:hidden"
      >
        ☰
      </button>
    </div>

    <div
      :class="[
        'lg:hidden overflow-hidden transition-all duration-300 ease-in-out',
        isMenuOpen ? 'max-h-96 opacity-100 tranlate-y-0' : 'max-h-0 opacity-0 -translate-y-2'
      ]"
    >
    <div class="bg-white shadow-lg">
      <ul class="flex flex-col">
        <li><NuxtLink to="#CPNS" class="block px-6 py-4">CPNS</NuxtLink></li>
        <li><NuxtLink to="#Masalah" class="block px-6 py-4">Masalah</NuxtLink></li>
        <li><NuxtLink to="#Solusi" class="block px-6 py-4">Solusi</NuxtLink></li>
        <li><NuxtLink to="#Benefit" class="block px-6 py-4">Benefit</NuxtLink></li>
        <li><NuxtLink to="#Paket" class="block px-6 py-4">Paket</NuxtLink></li>
        <li><NuxtLink to="#FAQ" class="block px-6 py-4">FAQ</NuxtLink></li>
      </ul>
    </div>
    </div>
  </nav>
</template>

<script setup>
// Pastikan baris ini berada tepat di dalam <script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isScrolled = ref(false);
const isMenuOpen = ref(false)

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