<template>
    <section class="py-12 px-4 my-10 items-center bg-orange-50 scroll-mt-24" id="Solusi">
        <div class="px-14 lg:px-48">
            <div class="max-w-2xl lg:max-w-3xl mx-auto">
                <h4 class="text-center font-bold text-2xl lg:text-3xl mb-4">Kami Membantu Kamu Belajar dengan Lebih Terarah</h4>
                <p class="mb-8 text-center">Persiapan CPNS bukan hanya soal banyak belajar, tetapi juga memahami kemampuan diri, membiasakan diri dengan sistem CAT, dan berlatih menggunakan soal yang sesuai standar terbaru.</p>
            </div>
            <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-8">
                <CardsSolusi 
                v-for="item in Solusi1"
                :Judul="item.Judul"
                :SubJudul="item.SubJudul"
                :button="item.button"
                :buttonText="item.buttonText"
                :icon="item.icon"
                :image="item.image"
                :image2="item.image2"
                :class="item.span"
                />
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import char from '~/assets/icon/chart.svg'
import book from '~/assets/icon/book.svg'
import trophy from '~/assets/icon/trophy.svg'
import CAT from '~/assets/images/CAT.jpg'
import winner from '~/assets/images/winner.jpg'

const Solusi1 = ref([
    {
        Judul:"Simulasi CAT dengan Batas Waktu Realistis",
        SubJudul:"Biasakan diri mengerjakan soal dalam kondisi yang menyerupai ujian sebenarnya sehingga lebih siap mengelola waktu saat tes berlangsung.",
        span: "lg:col-span-2",

        button: true,
        buttonText: "Coba Sekarang",
        image:CAT
    },
    {
        Judul:"Penilaian Otomatis dan Evaluasi Hasil",
        SubJudul:"Lihat hasil tryout secara langsung untuk mengetahui sejauh mana kesiapanmu menghadapi SKD.",
        icon: char
    },
    {
        Judul:"Soal Terupdate Sesuai Standar Terbaru",
        SubJudul:"Latihan menggunakan soal yang disusun mengikuti pola dan tingkat kesulitan terbaru.",
        icon: book
    },
    {
        Judul:"Pengalaman Tryout yang Mendekati Ujian Asli",
        SubJudul:"Membantu meningkatkan rasa percaya diri melalui simulasi yang dirancang mendekati ujian asli.",
        span: "lg:col-span-2",
        icon: trophy,
        image2:winner
    },
])
</script>