<template>
    <div class="font-titillium">
        <div class="w-[100%] relative">
            <img src="../../assets/img/portalsmkn4.jpeg" alt="" class="opacity-30 w-full" />
            <div class="absolute bottom-0 w-full h-full flex justify-center items-center">
                <p class="text-[2.5rem] font-semibold">Visi dan Misi</p>
            </div>
        </div>
        <p class="paddingX">
            <NuxtLink to="/">Beranda</NuxtLink> /
            <span class="text-[#2c52b3]">Visi dan Misi</span>
        </p>    
    </div>
    <div class="paddingX flex my-7 flex-col gap-10">
        <div class="visi">
            <p class="text-[1.5rem] font-semibold text-center">
                Visi
            </p>
            <hr>
            <p class="text-center mt-3">
                "TERWUJUDNYA LULUSAN YANG CERDAS, AKTIF, KOMPETITIF, ADAPTIF, DAN PRODUKTIF BERLANDASKAN IMAN DAN TAKWA"
                <br><br>
                "(CAKAP BERIMTAK)"
            </p>
        </div>
        <div class="misi">
            <p class="text-[1.5rem] font-semibold text-center">
                Misi
            </p>
            <hr>
            <ul class="list-decimal mt-3">
                <li v-for="visimisi in visimisi" :key="visimisi.id">
                    {{ visimisi.name }}
                </li>
            </ul>
        </div>
    </div>
</template>

<script setup>
const visimisi = ref([
    {id: 1, name: "Menyiapkan Sumber Daya Manusia yang cerdas dan kompeten baik hardskill maupun softskill."},
    {id: 2, name: "Meningkatkan dan mengembangkan aktifitas serta kreatifitas seluruh warga sekolah dalam berbagai kegiatan positif."},
    {id: 3, name: "Mewujudkan manajemen pengelolaan yang efektif, efesien, transparan, akuntabel dan layanan prima."},
    {id: 4, name: "Menumbuhkan dan mengembangkan potensi dan kemampuan Sumber Daya Manusia yang berdaya saing tinggi melalui berbagai kegiatan akademik maupun non akademik."},
    {id: 5, name: "Menyelenggarakan berbagai program kegiatan dalam upaya meningkatkan Sumber Daya Manusia yang mampu menyesuaikan dengan perkembangan."},
    {id: 6, name: "Mengembangkan sarana prasarana dan lingkungan sekolah yang menyenangkan sebagai wadah menumbuhkembangkan daya kreasi dan inovasi untuk menghasilkan produk teknologi tepat guna."},
    {id: 7, name: "Membangun jiwa wirausaha yang handal melalui pembelajaran Teaching Factory (TEFA) dan Kelas Industri."},
    {id: 8, name: "Menjalin dan mengembangkan kemitraan dengan Industri dan Dunia Kerja (IDUKA) serta lembaga lainnya yang relevan."},
    {id: 9, name: "Menanamkan dan membudayakan sikap dan perilaku yang baik pada aktivitas di sekolah maupun dalam kehidupan sehari-hari."},
])
</script>

<style lang="scss" scoped></style>