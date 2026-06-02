<template>
    <section class="py-12 px-4 my-10 items-center scroll-mt-24" id="Benefit">
        <div class="flex flex-col justify-center items-center">
            <h4 class="font-bold text-2xl lg:text-3xl mb-4">Kenapa Peserta Memilih Tryout Kami?</h4>

            <!-- mobile -->
            <div class="flex flex-col justify-center gap-4 lg:hidden items-stretch">
                <div class="flex justify-center w-full">
                    <img
                    src="~/assets/images/TryoutKami.png"
                    alt=""
                    class="w-64 sm:w-80 h-auto"
                    >
                </div>

                <UiBenefitCard
                v-for="item in [...benefit1, ...benefit2]"
                :key="item.Judul"
                :Judul="item.Judul"
                :subJudul="item.subJudul"
                />
            </div> 

            <!-- tablet & dekstop -->
                <div class="hidden lg:grid grid-cols-[1fr_auto_1fr] gap-8 items-center">
                    <div class="flex flex-col gap-8 mt-7">
                        <UiBenefitCard 
                        v-for="item in benefit1"
                        :Judul="item.Judul"
                        :subJudul="item.subJudul"
                        />
                    </div>
                    <div>
                        <img src="~/assets/images/TryoutKami.png" alt="" class="w-auto h-96">
                    </div>
                    <div class="flex flex-col gap-8 mt-7">
                        <UiBenefitCard 
                        v-for="item in benefit2"
                        :Judul="item.Judul"
                        :subJudul="item.subJudul"
                        />
                    </div>
                </div>
            </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const benefit1 = ref([
    {
        Judul:"Akurat dan Terpercaya",
        subJudul:"Soal disusun mengikuti standar terbaru."
    },
    {
        Judul:"Praktis dan Fleksibel",
        subJudul:"Akses dari mana saja tanpa batas lokasi."
    },
])
const benefit2 = ref([
    {
        Judul:"Evaluasi Instan",
        subJudul:"Nilai langsung muncul setelah tryout selesai."
    },
    {
        Judul:"Pengalaman Real Test",
        subJudul:"Simulasi dibuat menyerupai ujian asli."
    },
])
</script>
