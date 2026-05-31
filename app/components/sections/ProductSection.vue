<template>
  <section class="py-12 px-4 items-center" id="Paket">
    <div class="max-w-6xl mx-auto">
      <h2 class="text-3xl font-bold text-center">Pilih Paket CPNS</h2>
      <p class="text-center mb-8">Pilih paket yang paling sesuai dengan kebutuhanmu. Dan nikmati berbagai benefit dari Lulusmurni.com</p>
      <div class="flex justify-center">
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 items-stretch">
          <UiCardProduct 
            v-for="item in products" 
            :key="item.id" 
            :product="item" 
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
// Simulasi data yang datang (Nanti ganti dengan data dari API/Database)
const products = ref([
  {
    id: 1, // Pastikan gambar ada di folder public/images
    title: 'Gold CPNS',
    description: '1 Paket Soal SKD CPNS Paling Jitu.',
    price: 25000,
    benefit: ['Ada 1 Paket soal SKD CPNS Ter-JITU','Disesuikan dengan kisi-kisi Kemenpan RB dan BKN','Nilai Keluar Otomatis(Instant)','Timer Tryout','Bebas Mengulang Tanpa Batas','Evaluasi Jawaban Benar/Salah','Bisa Diakses Kapanpun & Dimanapun'],
    link: 'https://lulusmurni.com/product-detail/13'
  },
  {
    id: 2,
    title: 'Diamond CPNS',
    description: 'Ada 3 Paket soal berisi soal-soal terupdate dan akurat sesuai standar terbaru.',
    price: 35000,
    benefit:['Ada 3 Paket soal SKD CPNS JITU','Disesuikan dengan kisi-kisi Kemenpan RB dan BKN','Nilai Keluar Otomatis(Instant)','Timer Tryout','Bebas Mengulang Tanpa Batas','Evaluasi Jawaban Benar/Salah','Bisa Diakses Kapanpun & Dimanapun'],
    link:'https://lulusmurni.com/product-detail/14'
  },
  {
    id: 3,
    title: 'All-in CPNS',
    description: 'Paket ini berisi 5 Paket Tryout dengan soal-soal terupdate dan akurat sesuai standar terbaru.',
    price: 50000,
    benefit:['Ada 5 Paket soal SKD CPNS Ter-JITU','Disesuikan dengan kisi-kisi Kemenpan RB dan BKN','Nilai Keluar Otomatis(Instant)','Timer Tryout','Bebas Mengulang Tanpa Batas','Dapat E-Book Latihan Soal','Evaluasi Jawaban Benar/Salah','Bisa Diakses Kapanpun & Dimanapun'],
    link: 'https://lulusmurni.com/product-detail/15'
  },
])
</script>