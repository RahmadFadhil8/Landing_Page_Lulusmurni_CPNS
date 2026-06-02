<template>
  <div class="max-w-sm w-full bg-orange-100 p-1 rounded-xl">
    
    <div class="bg-orange-100 rounded-[1.25rem] p-8 flex flex-col gap-5">
      
      <div class="flex flex-col gap-2">
        <h5 class="font-bold text-lg text-blue-950 leading-tight">
          {{ Judul }}
        </h5>
        
        <div class="w-16 h-1 bg-black rounded-full mt-1 mb-2"></div>
        
        <p class="text-sm leading-relaxed font-light">
          {{ SubJudul }}
        </p>
      </div>
    </div>
  </div>
</template>

<script setup>
defineProps({
  Judul: String,
  SubJudul: String,
})
</script>