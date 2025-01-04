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
        <p class="text-[2.5rem] font-semibold">Sejarah Singkat</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Sejarah</span>
    </p>
    <div class="paddingX flex gap-10 mb-7 justify-around">
      <div class="w-[50%]">
        <div class="relative inline-block mb-2">
          <span class="relative text-[2rem]"> Awal Mula Berdirinya </span>
          <div class="absolute bottom-0 left-0 w-36 h-[1px] bg-current"></div>
        </div>
        <p class="text-justify tracking-wide">
          Sejalan dengan Program Pemerintah dibidang pendidikan Menengah
          Kejuruan pada saat itu yakni pemerataan akses ditambah pula dengan
          banyaknya keinginan masyarakat yang mengharapkan adanya SMK Negeri di
          daerah Kecamatan Purbaratu Kota Tasikmalaya, terutama untuk menampung
          tamatan dari SLTP yang ingin melanjutkan ke SMK maka beberapa tokoh
          masyarakat, unsur pejabat pemerintah di Kecamatan Purbaratu Kota
          Tasikmalaya mengusulkan kepada pemerintah Kota Tasikmalaya dan
          Pemerintah Provinsi Jawa Barat, agar berdirinya SMK Negeri di
          Kecamatan Purbaratu Kota Tasikmalaya. <br />
          <br />
          Setelah melalui perjuangan yang sangat panjang dari berbagai pihak
          khususnya Disdik Kota Tasikmalaya dan pihak-pihak terkait lainnya
          sesuai prosedur dan ketentuan yang berlaku pada waktu itu dengan
          mengucapkan syukur Alhamdulillah akhirnya pada tahun pelajaran
          2010/2011 SMK Negeri 4 Tasikmalaya mulai berdiri, pada awalnya membuka
          Kompetensi Keahlian Teknik Komputer dan Jaringan dengan pendaftar
          peserta Didik Baru pada waktu itu berjumlah 44 orang. Pada awalnya
          tempat belajar menumpang di SMP Negeri 17 Kota Tasikmalaya, dan
          sekolah induknya adalah SMK Negeri 2 Kota Tasikmalaya, Untuk Tenaga
          pendidik dan Tenaga Kependidikan masih dibantu sepenuhnya oleh kedua
          sekolah tersebut. <br />
          <br />
          Pada tahun 2012 keluarlah surat Izin Pendirian berdasarkan keputusan
          kepala Badan Pelayanan Perizinan Terpadu Kota Tasikmalaya No.
          420/9/SK-BPPT/2012 Tanggal 06 Februari 2012.
        </p>
      </div>
      <div class="mb-4">
        <div class="relative inline-block mb-2">
          <span class="relative text-[2rem]">
            Perkembangan Infrastruktur Pertahun
          </span>
          <div class="absolute bottom-0 left-0 w-36 h-[1px] bg-current"></div>
        </div>
        <table>
          <thead class="border border-black">
            <tr>
              <td
                class="border border-white p-2 text-center bg-[#11224e] text-white"
              >
                Tahun
              </td>
              <td
                class="border border-white p-2 text-center bg-[#11224e] text-white"
              >
                Ruang Kelas
              </td>
              <td
                class="border border-white p-2 text-center bg-[#11224e] text-white"
              >
                Program Keahlian
              </td>
              <td
                class="border border-white p-2 text-center bg-[#11224e] text-white"
              >
                Jumlah Siswa
              </td>
              <td
                class="border border-white p-2 text-center bg-[#11224e] text-white"
              >
                Pimpinan
              </td>
            </tr>
          </thead>
          <tbody class="border border-black">
            <tr v-for="(item, i) in items" :key="i">
              <td class="border border-black p-1 text-center">
                {{ item.tahun }}
              </td>
              <td class="border border-black p-1 text-center">
                {{ item.kelas }}
              </td>
              <td class="border border-black p-1 text-center">
                {{ item.proke }}
              </td>
              <td class="border border-black p-1 text-center">
                {{ item.siswa }}
              </td>
              <td class="border border-black p-1 text-center">
                {{ item.pimpinan }}
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script setup>
const items = ref([
  {
    tahun: "2010/2011",
    kelas: "di SMPN 17",
    proke: "TKJ",
    siswa: "44",
    pimpinan: "PLT. Drs. H.Ario Wiguno, M.MPd",
  },
  {
    tahun: "2011/2012",
    kelas: "di SMPN 17",
    proke: "TKJ",
    siswa: "?",
    pimpinan: "PLT. Drs. H.Ario Wiguno, M.MPd",
  },
  {
    tahun: "2012/2013",
    kelas: "di SMKN 4",
    proke: "TKJ",
    siswa: "?",
    pimpinan: "PLT. H. Edy Sugandi, MM",
  },
  {
    tahun: "2013/2014",
    kelas: "di SMKN 4",
    proke: "TKJ",
    siswa: "?",
    pimpinan: "PLT. H. Edy Sugandi, MM",
  },
  {
    tahun: "2014/2015",
    kelas: "di SMKN 4",
    proke: "TKJ",
    siswa: "268",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2015/2016",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "461",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2016/2017",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "693",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2017/2018",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "1021",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2018/2019",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "1093",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2019/2020",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "1116",
    pimpinan: "Drs. H. Desnueri",
  },
  {
    tahun: "2020/2021",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "1150",
    pimpinan: "Didah S Sukanda, S.Pd, M.Pd.",
  },
  {
    tahun: "2021/2022",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM",
    siswa: "1150",
    pimpinan: "	Kurniawan, S.Pd, M.Pd.",
  },
  {
    tahun: "2022/2023",
    kelas: "di SMKN 4",
    proke: "TKJ, RPL, TSM, TOI, DKV",
    siswa: "1124",
    pimpinan: "	Kurniawan, S.Pd, M.Pd.",
  },
]);
</script>

<style scoped></style>
