<template>
  <div class="font-titillium">
    <div class="w-[100%] relative">
      <img
        src="../assets/img/portalsmkn4.jpeg"
        alt=""
        class="opacity-30 w-full"
      />
      <div
        class="absolute bottom-0 w-full h-full flex justify-center items-center"
      >
        <p class="text-[2.5rem] font-semibold">Artikel</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Artikel</span>
    </p>
    <div class="flex paddingX">
      <div class="Content w-[70%] mb-7">
        <div class="relative inline-block">
          <span class="relative text-[2rem]">
          Berita
          </span>
          <div class="absolute bottom-0 left-0 w-10 h-[1px] bg-current"></div>
        </div>
        <ol class="flex flex-col gap-5">
          <li>
            <p class="font-medium text-[#2c52b3] hover:underline">
              <a href="https://www.smkn4-tsm.sch.id/article/berita"> Informasi PPDB Tahap 2 Tahun 2020 SMKN 4 Tasikmalaya </a>
            </p>
            <p class="text-[#11224eaa]">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illum
              nihil harum praesentium fugit amet necessitatibus
            </p>
          </li>
          <li>
            <p class="font-medium text-[#2c52b3] hover:underline">
              <a href="https://www.smkn4-tsm.sch.id/article/berita"> Daftar Ulang PPDB SMKN 4 Tasikmalaya Tahap 1 Tahun 2020 </a>
            </p>
            <p class="text-[#11224eaa]">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit. Illum
              nihil harum praesentium fugit amet necessitatibus
            </p>
          </li>
        </ol>
      </div>
      <div class="Sidebar w-[30%]">
        <div class="relative inline-block">
          <span class="relative text-[2rem]">Pengumuman </span>
          <div class="absolute bottom-0 left-0 w-28 h-[1px] bg-current"></div>
        </div>
        <ol class="flex flex-col gap-5">
          <li>
            <p class="font-medium text-[#2c52b3] hover:underline">
              <a href="https://www.smkn4-tsm.sch.id/article/berita"> Informasi PPDB Tahap 2 Tahun 2020 SMKN 4 Tasikmalaya </a>
            </p>
            <p class="text-[#11224eaa]">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            </p>
          </li>
          <li>
            <p class="font-medium text-[#2c52b3] hover:underline">
              <a href="https://www.smkn4-tsm.sch.id/article/berita"> Daftar Ulang PPDB SMKN 4 Tasikmalaya Tahap 1 Tahun 2020 </a>
            </p>
            <p class="text-[#11224eaa]">
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
            </p>
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead ({ title: "Artikel - SMKN 4 Tasikmalaya" })

</script>

<style scoped></style>
