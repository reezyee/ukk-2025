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
        <p class="text-[2.5rem] font-semibold">Ekstrakurikuler</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Ekstrakurikuler</span>
    </p>
    <div class="paddingX my-7">
      <div class="flex gap-5 flex-wrap justify-around">
        <div v-for="(ekskul, i) in ekskul" :key="i" class="group card shadow-md border-t p-5">
          <div class="cardHead w-40">
            <img :src="ekskul.src" :alt="ekskul.name" class="bg-contain group-hover:scale-105 group-hover:transition-all">
          </div>
          <div class="cardBody w-40 text-center">
            {{ ekskul.name }}
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead ({ title: "Ekstrakurikulerb - SMKN 4 Tasikmalaya" })

import ec from "../../assets/img/ekskul/ec.jpg";
import paskibra from "../../assets/img/ekskul/paskibra.jpg";
import pub from "../../assets/img/ekskul/pub.jpg";
import pramuka from "../../assets/img/ekskul/pramuka.jpg";
import itc from "../../assets/img/ekskul/itc.jpg";
import irma from "../../assets/img/ekskul/irma.jpg";
import basket from "../../assets/img/ekskul/basket.jpg";
import futsal from "../../assets/img/ekskul/futsal.jpg";
import bulutangkis from "../../assets/img/ekskul/bulutangkis.jpg";
import dance from "../../assets/img/ekskul/dance.jpg";
import cj from "../../assets/img/ekskul/cj.jpg";
import laskar from "../../assets/img/ekskul/laskar.jpg";
import osis from "../../assets/img/ekskul/osis.jpg";
import pks from "../../assets/img/ekskul/pks.jpg";
import srl from "../../assets/img/ekskul/srl.jpg";
import plh from "../../assets/img/ekskul/plh.jpg";
import pd from "../../assets/img/ekskul/pd.jpg";
import pmr from "../../assets/img/ekskul/pmr.jpg";
import sepakbola from "../../assets/img/ekskul/sepakbola.jpg";
import voli from "../../assets/img/ekskul/voli.jpg";

const ekskul = ref([
  { src: basket, name: "Basketball" },
  { src: bulutangkis, name: "Bulu Tangkis" },
  { src: cj, name: "Cinematografi" },
  { src: dance, name: "Dance" },
  { src: ec, name: "English Club" },
  { src: futsal, name: "Futsal" },
  { src: irma, name: "Ikatan Remaja Masjid" },
  { src: itc, name: "IT Club" },
  { src: laskar, name: "Gerakan Laskar Pustaka" },
  { src: osis, name: "Organisasi Siswa Intra Sekolah" },
  { src: paskibra, name: "Pengibar Upacara Bendera" },
  { src: pd, name: "Perisai Diri" },
  { src: pub, name: "Pendidikan Untuk Bela Negara" },
  { src: pks, name: "Patroli Keamanan Sekolah" },
  { src: plh, name: "Pecinta Lingkungan Hidup" },
  { src: pmr, name: "Palang Merah Remaja" },
  { src: pramuka, name: "Pramuka" },
  { src: sepakbola, name: "Sepak Bola" },
  { src: srl, name: "Safety Riding Lab" },
  { src: voli, name: "Volley Ball" },
]);
</script>

<style scoped></style>
