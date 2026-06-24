<template>
    <UiCard variant="Solusi">
        <div class="w-full p-1 flex flex-col">    
            <div class="h-full p-8 flex flex-col gap-5">
                <div v-if="image || image2" class="flex flex-col lg:flex-row gap-2">
                    <div class="shrink-0">
                        <img 
                            v-if="image2"
                            :src="image2" 
                            :alt="Judul"
                            class="rounded-xl w-full object-cover hidden lg:block"
                        >
                    </div>

                    <div v-if="image" class="flex-1 mr-4">
                        <div class="flex items-center gap-4">
                            <img v-if="icon" :src="icon" :alt="Judul" class="h-6 w-6">
                            <h5 class="font-bold text-lg text-blue-950 leading-tight">
                            {{ Judul }}
                            </h5>
                        </div>

                        <div class="w-16 h-1 bg-black rounded-full mt-1 mb-2"></div>
                        
                        <p class="text-sm leading-relaxed font-light mb-4">
                            {{ SubJudul }}
                        </p>
                        
                        <UiButton v-if="button" class="font-bold text-white">
                            {{ buttonText }}
                        </UiButton>
                    </div>

                    <div v-else class="flex-1 ml-4">
                        <div class="flex items-center gap-4">
                            <img v-if="icon" :src="icon" :alt="Judul" class="h-6 w-6">
                            <h5 class="font-bold text-lg text-blue-950 leading-tight">
                            {{ Judul }}
                            </h5>
                        </div>

                        <div class="w-16 h-1 bg-black rounded-full mt-1 mb-2"></div>
                        
                        <p class="text-sm leading-relaxed font-light mb-4">
                            {{ SubJudul }}
                        </p>
                        
                        <UiButton v-if="button" class="font-bold text-white">
                            {{ buttonText }}
                        </UiButton>
                    </div>
                    
                    <div class="shrink-0">
                        <img 
                            v-if="image"
                            :src="image" 
                            :alt="Judul"
                            class="rounded-xl w-full object-cover hidden lg:block"
                        >
                    </div>
                </div>

                <!-- Card biasa tanpa gambar -->
                <div v-else>
                    <div class="flex items-center gap-4 mb-4">
                        <img
                            v-if="icon"
                            :src="icon"
                            :alt="Judul"
                            class="h-6 w-6"
                        >

                        <h5 class="font-bold text-lg text-blue-950">
                            {{ Judul }}
                        </h5>
                    </div>

                    <div class="w-16 h-1 bg-black rounded-full mb-4"></div>

                    <p class="text-sm leading-relaxed font-light">
                        {{ SubJudul }}
                    </p>
                </div>
            </div>
        </div>
    </UiCard>
</template>

<script setup lang="ts">
defineProps({
  Judul: String,
  SubJudul: String,
  span: String,
  button: Boolean,
  image: String,
  image2: String,
  icon: String,
  buttonText: String
})
</script>