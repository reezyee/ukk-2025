<template>
    <!-- <div class=""> -->
    <div class="bg-white font-titillium flex justify-between items-center paddingX border-b">
        <div class="">
            <NuxtLink to="/" class="flex items-center gap-5">
                <img src="../assets/img/logo.png" alt="Logo SMKN 4 Tasikmalaya" class="w-20">
                <p class="text-[2.5rem] font-bold text-[#11224e]">SMKN 4 Tasikmalaya</p>
            </NuxtLink>
        </div>
        <div class="flex gap-5">
            <ul class="flex items-center gap-5 justify-center">
                <li v-for="medsos in medsos" :key="medsos.id"
                    class="group bg-transparent border rounded-full w-10 h-10 flex justify-center items-center pt-1 hover:bg-[#11224e]">
                    <a :href="medsos.path" :title="medsos.name">
                        <Icon :name="medsos.src" size="1.5rem" class="group-hover:text-white" />
                    </a>
                </li>
            </ul>
            <ul class="flex items-center gap-5 border-s ps-7">
                <li v-for="other in others" :key="other.id" class="flex gap-3">
                    <Icon :name="other.src" size="1.5rem" />
                    <a :href="other.path" :title="other.name">
                        {{ other.subject }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
    <div class="Navbar paddingX shadow-md sticky top-0 bg-white z-20">
        <ul class="flex gap-7 justify-end">
            <li>
                <NuxtLink to="/">
                    Beranda
                </NuxtLink>
            </li>
            <li>
                <NuxtLink to="/artikel">
                    Artikel
                </NuxtLink>
            </li>
            <li class="group inline-block">
                <div class="flex items-center cursor-pointer">
                    <p>
                        Profil
                    </p>
                    <Icon name="material-symbols:keyboard-arrow-down" size="1rem" class="group-hover:rotate-180" />
                </div>
                <ul class="absolute hidden group-hover:block ">
                    <li v-for="profile in profiles" :key="profile.id" class="p-2 hover:bg-[#dadada] bg-white">
                        <NuxtLink :to="profile.path">{{ profile.name }}</NuxtLink>
                    </li>
                </ul>
            </li>
            <li class="group inline-block">
                <div class="flex items-center cursor-pointer">
                    <p>
                        Siswa
                    </p>
                    <Icon name="material-symbols:keyboard-arrow-down" size="1rem" class="group-hover:rotate-180" />
                </div>
                <ul class="absolute hidden group-hover:block ">
                    <li v-for="student in students" :key="student.id" class="p-2 hover:bg-[#dadada] bg-white">
                        <NuxtLink :to="student.path">{{ student.name }}</NuxtLink>
                    </li>
                </ul>
            </li>
            <li>
                <NuxtLink to="/galeri">
                    Galeri
                </NuxtLink>
            </li>
        </ul>
    </div>
    <!-- </div> -->
</template>

<script setup>
const medsos = ref([
    { id: 1, path: "https://tiktok.com/smk4tasikmalaya", name: "Tik Tok", src: "ic:sharp-tiktok" },
    { id: 2, path: "https://instagram.com/smkn4tasimalaya", name: "Instagram", src: "hugeicons:instagram" },
    { id: 3, path: "https://youtube.com/@smkn4tasikmalayamediaoffic704", name: "Youtube", src: "uil:youtube" },
    { id: 4, path: "https://x.com/4_smkn", name: "X", src: "hugeicons:new-twitter" },
])

const others = ref([
    { id: 1, src: "ion:ios-telephone", name: "Nomor Telepon Sekolah", path: "tel:+62265312059", subject: "+62265312059" },
    { id: 2, src: "material-symbols:mail", name: "Email Sekolah", path: "mailto:info@smkn4-tsm.sch.id", subject: "info@smkn4-tsm.sch.id" },
])

const profiles = ref([
    { id: 1, path: "/profil/sejarah" ,name: "Sejarah" },
    { id: 2, path: "/profil/identitas" ,name: "Identitas Sekolah" },
    { id: 3, path: "/profil/visimisi" ,name: "Visi dan Misi" },
    { id: 4, path: "/profil/gustaf" ,name: "Guru dan Staff" },
])

const students = ref([
    { id: 1, name: "Kejuruan", path: "/siswa/proke"},
    { id: 2, name: "Ekstrakurikuler", path: "/siswa/ekskul"},
])
</script>

<style scoped></style>