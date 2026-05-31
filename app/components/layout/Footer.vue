<template>
    <footer class="px-40 py-10">
        <div class="grid grid-cols-2">
            <div class="mr-12 text-justify">
                <img src="~/assets/images/lulusMurniASN .png" alt="logo" class="h-13 w-auto mb-4">
                <p>
                    Lulusmurni.com adalah platform ujian CAT/CBT, tryout, dan sertifikasi berbasis online yang praktis, fleksibel, dan terpercaya. Dirancang untuk memberikan pengalaman belajar interaktif, mendukung persiapanmu secara maksimal, dan membantu meraih karir impian.
                </p>
                <div class="flex gap-2 mt-4">
                    <NuxtLink to="https://www.facebook.com/people/Lulusmurnidotcom/61575286704690/?_rdc=1&_rdr#"><img src="~/assets/icon/ic_baseline-facebook.svg" alt=""></NuxtLink>
                    <NuxtLink to="https://www.instagram.com/lulusmurnidotcom/"><img src="~/assets/icon/mdi_instagram.svg" alt=""></NuxtLink>
                    <NuxtLink to="https://x.com/Lulusmurnicom"><img src="~/assets/icon/mdi_twitter.svg" alt=""></NuxtLink>
                </div>
            </div>
            <div class="grid grid-cols-3 gap-5">
                <ul class="flex flex-col gap-4">
                    <li><NuxtLink to="/">Apa itu ASN atau CPNS?</NuxtLink></li>
                    <li><NuxtLink to="/">Portofolio</NuxtLink></li>
                    <li><NuxtLink to="/">Benefit</NuxtLink></li>
                    <li><NuxtLink to="/">Pilihan Paket</NuxtLink></li>
                    <li><NuxtLink to="/">Testimoni</NuxtLink></li>
                    <li><NuxtLink to="/">FAQ</NuxtLink></li>
                </ul>

                <div class="flex flex-col gap-4 justify-self-center">
                    <p>Jam Operasional</p>
                    <p>Setiap Hari</p>
                    <p>09.00 - 21.00</p>
                </div>

                <div class="flex flex-col gap-4">
                    <p>Hubungi Kami</p>
                    <div class="">
                        <p>Kontak</p>
                        <div class="flex gap-3 mt-2">
                            <img src="~/assets/icon/ic_baseline-phone.svg" alt="">
                            <p class="font-bold">0822-1322-2085</p>
                        </div>
                    </div>
                    <div class="flex gap-3">
                        <img src="~/assets/icon/ic_baseline-email.svg" alt="">
                        <p class="font-bold">halo@lulusmurni.com</p>
                    </div>
                </div>
            </div>
        </div>
        <div>
            <div class="flex justify-center pt-3 lg:pt-5 border-t-2 border-black/80 text-[12px] lg:mt-10">
                <p>Copyright PT Cendikia Lentera Bangsa 2026 All rights reserved.</p>
            </div>
        </div>
    </footer>
</template>