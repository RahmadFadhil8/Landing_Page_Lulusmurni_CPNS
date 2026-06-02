<template>
    <section class="py-12 px-4 my-10 items-center bg-orange-50 scroll-mt-24" id="Solusi">
        <div class="px-48">
            <div class="grid grid-cols-2 gap-4 mb-4">
                <div>
                    <h4 class="font-bold text-3xl mb-4">Kami Membantu Kamu Belajar dengan Lebih Terarah</h4>
                    <p class="mb-4">Persiapan CPNS bukan hanya soal banyak belajar, tetapi juga memahami kemampuan diri, membiasakan diri dengan sistem CAT, dan berlatih menggunakan soal yang sesuai standar terbaru.</p>
                    <UiButton />
                </div>
                <div class="flex flex-col justify-end items-end">
                    <UiSolusi 
                    v-for="item in Solusi1"
                    :Judul="item.Judul"
                    :SubJudul="item.SubJudul"
                    />
                </div>
            </div>
            <div class="grid grid-cols-3 gap-4">
                <UiSolusi 
                v-for="item in Solusi2"
                :Judul="item.Judul"
                :SubJudul="item.SubJudul"
                />
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