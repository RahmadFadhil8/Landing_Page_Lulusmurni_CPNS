<template>
    <section class="py-12 px-4 my-10 items-center bg-orange-50 scroll-mt-24" id="Solusi">
        <div class="px-14 lg:px-48">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mb-8">
                <div class="text-center lg:text-left">
                    <h4 class="font-bold text-2xl lg:text-3xl mb-4">Kami Membantu Kamu Belajar dengan Lebih Terarah</h4>
                    <p class="mb-4">Persiapan CPNS bukan hanya soal banyak belajar, tetapi juga memahami kemampuan diri, membiasakan diri dengan sistem CAT, dan berlatih menggunakan soal yang sesuai standar terbaru.</p>
                    <div class="flex justify-center lg:justify-start">
                        <UiButton />
                    </div>
                </div>
                <div class="hidden lg:flex lg:justify-end items-end">
                    <UiSolusi 
                    v-for="item in Solusi1"
                    :Judul="item.Judul"
                    :SubJudul="item.SubJudul"
                    />
                </div>
            </div>
            <div class="flex justify-center items-center">
                <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8">
                    <UiSolusi 
                    v-for="item in Solusi2"
                    :Judul="item.Judul"
                    :SubJudul="item.SubJudul"
                    />
                    <UiSolusi 
                        v-for="item in Solusi1"
                        :Judul="item.Judul"
                        :SubJudul="item.SubJudul"
                         class="lg:hidden"/>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const Solusi1 = ref([
    {
        Judul:"Simulasi CAT dengan Batas Waktu Realistis",
        SubJudul:"Biasakan diri mengerjakan soal dalam kondisi yang menyerupai ujian sebenarnya sehingga lebih siap mengelola waktu saat tes berlangsung."
    },
])

const Solusi2 = ref([
    {
        Judul:"Penilaian Otomatis dan Evaluasi Hasil",
        SubJudul:"Lihat hasil tryout secara langsung untuk mengetahui sejauh mana kesiapanmu menghadapi SKD."
    },
    {
        Judul:"Soal Terupdate Sesuai Standar Terbaru",
        SubJudul:"Latihan menggunakan soal yang disusun mengikuti pola dan tingkat kesulitan terbaru."
    },
    {
        Judul:"Pengalaman Tryout yang Mendekati Ujian Asli",
        SubJudul:"Membantu meningkatkan rasa percaya diri melalui simulasi yang dirancang mendekati ujian asli."
    },
])
</script>