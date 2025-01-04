<template>
  <div class="font-titillium">
    <div class="w-[100%] relative">
      <img
        src="../../assets/img/portalsmkn4.jpeg"
        alt=""
        class="opacity-30 w-full"
      />
      <div
        class="absolute bottom-0 w-full h-full flex justify-center items-center"
      >
        <p class="text-[2.5rem] font-semibold">Identitas Sekolah</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Identitas Sekolah</span>
    </p>
    <div class="paddingXY flex justify-around items-center">
      <img src="../../assets/img/logo.png" alt="" class="w-72 h-80 bg-contain drop-shadow-2xl" />
      <table class="IdentitasSekolah">
        <tr
          v-for="(identitas, i) in identitas"
          :key="i"
          :class="i % 2 === 0 ? 'bg-white' : 'bg-[#c4d5ff]'"
        >
          <td class="px-2 py-1">{{ identitas.name }}</td>
          <td class="w-10 text-center">:</td>
          <td class="px-2 py-1">{{ identitas.value }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script setup>
const identitas = ref([
  { name: "Nama Sekolah", value: "SMK Negeri 4 Kota Tasikmalaya" },
  { name: "NPSN", value: "20276063" },
  { name: "Nomor Statistik Sekolah", value: "401327810004" },
  {
    name: "Alamat",
    value:
      "Jl Depok RT 02 RW 05, Kel. Sukamenak, Kec. Purbaratu, Kota Tasikmalaya, Provinsi Jawa Barat",
  },
  { name: "Pendirian", value: "" },
  { name: "Nomor SK Pendirian", value: "420/9/SK-BPPT/2012" },
  { name: "Tanggal", value: "06 Februari 2012" },
  { name: "Akreditasi", value: "A (UNGGUL) dengan Nilai 92" },
  {
    name: "Nilai Satuan Pendidikan",
    value: "92",
  },
  { name: "Prog. Keahlian Teknik Otomotif", value: "91" },
  { name: "Prog. Keahlian Teknik Komputer dan Informatika ", value: "92" },
]);
</script>

<style scoped></style>
