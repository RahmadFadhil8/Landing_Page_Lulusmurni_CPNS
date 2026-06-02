<template>
    <section class="py-12 px-4 my-10 items-center scroll-mt-24" id="Masalah">
        <div class="flex flex-col justify-center items-center px-48">
            <h4 class="font-bold text-3xl mb-4">Masih Belajar CPNS Tanpa Tahu Seberapa Siap Kamu?</h4>
            <p class="mb-10 text-center">Banyak peserta CPNS menghabiskan waktu berbulan-bulan untuk belajar, namun tetap merasa kurang siap saat hari ujian tiba. Bukan karena kurang usaha, tetapi karena belum pernah merasakan simulasi yang benar-benar menyerupai tes CAT sebenarnya.</p>
            <div class="grid grid-cols-4 gap-6">
                <UiCardMasalah 
                v-for="item in Masalah"
                :Judul="item.Judul"
                :SubJudul="item.SubJudul"
                />
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const Masalah = ref([
    {
        Judul:"Kesulitan Mengatur Waktu",
        SubJudul:"Saat ujian berlangsung, waktu terasa jauh lebih cepat daripada saat latihan biasa."
    },
    {
        Judul:"Tidak Tahu Kemampuan Sebenarnya",
        SubJudul:"Belajar tanpa evaluasi membuat sulit mengetahui apakah kemampuan sudah memenuhi target."
    },
    {
        Judul:"Belum Terbiasa dengan Pola Soal",
        SubJudul:"Perubahan pola dan tingkat kesulitan soal sering membuat peserta kehilangan banyak poin."
    },
    {
        Judul:"Kurang Percaya Diri Saat Ujian",
        SubJudul:"Kurangnya pengalaman simulasi membuat peserta lebih mudah gugup ketika tes berlangsung."
    },
])
</script>