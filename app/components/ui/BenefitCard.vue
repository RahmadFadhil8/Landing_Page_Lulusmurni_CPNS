<template>
    <div class="flex gap-2 bg-green-100 px-6 py-4 rounded-lg">
        <div>
            <img src="~/assets/icon/green-check.svg" alt="" class="mt-1.5 w-7 lg:mt-0.5">
        </div>
        <div>
            <h5 class="font-bold text-sm lg:text-base">{{ Judul }}</h5>
            <p class="text-xs lg:text-sm">{{ subJudul }}</p>
        </div>
    </div>
</template>
<script setup>
defineProps({
  Judul: String,
  subJudul: String,
})
</script>