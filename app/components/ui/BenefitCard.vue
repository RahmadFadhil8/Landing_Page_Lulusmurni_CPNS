<template>
    <div class="flex gap-2 bg-green-100 px-6 py-4 rounded-lg">
        <div>
            <img src="~/assets/icon/green-check.svg" alt="" class="mt-0.5">
        </div>
        <div>
            <h5 class="font-bold">{{ Judul }}</h5>
            <p>{{ subJudul }}</p>
        </div>
    </div>
</template>
<script setup>
defineProps({
  Judul: String,
  subJudul: String,
})
</script>