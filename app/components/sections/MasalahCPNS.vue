<template>
    <section class="py-12 px-4 my-10 items-center scroll-mt-24" id="Masalah">
        <div class="flex flex-col lg:justify-center items-center px-14 lg:px-48">
            <div class="max-w-2xl lg:max-w-3xl mx-auto">
                <h4 class="font-bold text-2xl text-center lg:text-3xl mb-4">Masih Belajar CPNS Tanpa Tahu Seberapa Siap Kamu?</h4>
                <p class="mb-10 text-center text-base">Banyak peserta CPNS menghabiskan waktu berbulan-bulan untuk belajar, namun tetap merasa kurang siap saat hari ujian tiba. Bukan karena kurang usaha, tetapi karena belum pernah merasakan simulasi yang benar-benar menyerupai tes CAT sebenarnya.</p>
            </div>
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 items-stretch">
                <CardsMasalah 
                v-for="item in Masalah"
                :judul="item.judul"
                :subJudul="item.subJudul"
                :icon="item.icon"
                />
            </div>
        </div>
    </section>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import clock from '~/assets/icon/clock.svg'
import clipboard from '~/assets/icon/clipboard.svg'
import chart from '~/assets/icon/chart.svg'
import shield from '~/assets/icon/shield.svg'

const Masalah = ref([
    {
        icon: clock,
        judul:"Kesulitan Mengatur Waktu",
        subJudul:"Saat ujian berlangsung, waktu terasa jauh lebih cepat daripada saat latihan biasa."
    },
    {
        icon:chart,
        judul:"Tidak Tahu Level Kemampuan",
        subJudul:"Belajar tanpa evaluasi membuat sulit mengetahui apakah kemampuan sudah memenuhi target."
    },
    {
        icon:clipboard,
        judul:"Belum Terbiasa dengan Pola Soal",
        subJudul:"Perubahan pola dan tingkat kesulitan soal sering membuat peserta kehilangan banyak poin."
    },
    {
        icon:shield,
        judul:"Kurang Percaya Diri Saat Ujian",
        subJudul:"Kurangnya pengalaman simulasi membuat peserta lebih mudah gugup ketika tes berlangsung."
    },
])
</script>