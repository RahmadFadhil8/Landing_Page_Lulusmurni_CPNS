<template>
    <section class="py-12 px-4 my-10 items-center scroll-mt-24" id="FAQ">
        <div class="max-w-5xl mx-auto">
            <h2 class="text-2xl lg:text-3xl font-bold text-center mb-6">Pertanyaan yang Sering Diajukan</h2>
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 items-center">
                <div class="flex flex-col gap-4">
                    <div class="space-y-4">
                        <div v-for="(item, index) in Faq" 
                    :key="index" class="border rounded-lg bg-white shadow-sm overflow-hidden transition-colors duration-300 border-gray-200">
                            <button @click="TombolFAQ(index)" class="w-full flex justify-between items-center px-6 py-4 cursor-pointer hover:bg-gray-50 transition-colors">
                                <h3 class="text-sm lg:text-base font-bold">{{ item.Pertanyaan }}</h3>
                                <img src="~/assets/icon/faq-icon.svg" class="transition-transform duration-300":class="activeIndex === index ? 'rotate-90' : ''" alt="icon">
                            </button>
                            
                            <div v-show="activeIndex === index" class="p-3 pl-4 pt-3 lg:pl-6 bg-gray-100">
                                <p class="text-sm lg:text-base">{{ item.Jawaban }}</p>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="hidden lg:flex justify-center lg:justify-end">
                    <img src="~/assets/images/Gambar ASN2.png" alt="" class="h-64 md:h-80 lg:h-80 w-auto">
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped>
.animate-fade-in {
  animation: fadeIn 0.3s ease-in-out;
}
@keyframes fadeIn {
  from { opacity: 0; transform: translateY(-10px); }
  to { opacity: 1; transform: translateY(0); }
}
</style>

<script setup>
import { ref } from 'vue';

const activeIndex = ref(null);

const Faq = ref([
    {
        Pertanyaan:"Apakah soal sesuai CAT terbaru?",
        Jawaban:"Ya, soal terus diperbarui mengikuti pola dan sistem terbaru CPNS."
    },
    {
        Pertanyaan:"Apakah bisa diakses lewat HP?",
        Jawaban:"Bisa. Platform dapat digunakan melalui smartphone maupun laptop."
    },
    {
        Pertanyaan:"Apakah ada pembahasan soal?",
        Jawaban:"Pembahasan Soal berbeda untuk setiap paket dan dapat dilihat pada detail paket."
    },
    {
        Pertanyaan:"Apakah tryout bisa diulang?",
        Jawaban:"Ya, Bebas Mengulang Tanpa Batas."
    },

])

const TombolFAQ = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index;
};

</script>