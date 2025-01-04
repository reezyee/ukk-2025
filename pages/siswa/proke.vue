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
        <p class="text-[2.5rem] font-semibold">Kejuruan</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Kejuruan</span>
    </p>
    <div class="paddingX my-7 flex flex-col gap-5">
      <div class="relative inline-block">
        <span class="relative text-[2rem]">Program Keahlian</span>
        <div class="absolute bottom-0 left-0 w-36 h-[1px] bg-current"></div>
      </div>
      <div class="flex gap-5">
        <div
          v-for="(logo, i) in logos"
          :key="i"
          class="card w-80 shadow-md border-t rounded-xl"
        >
          <div class="cardHead h-80 flex flex-col items-center justify-around">
            <img :src="logo.src" :alt="logo.name" class="h-56 bg-contain" />
          </div>
          <div class="cardBody text-center p-2">
            <p class="text-[1.2rem] font-semibold">{{ logo.name }}</p>
          </div>
        </div>
      </div>
      <div class="relative inline-block">
        <span class="relative text-[2rem]">Kosentrasi Keahlian</span>
        <div class="absolute bottom-0 left-0 w-36 h-[1px] bg-current"></div>
      </div>
      <div class="">
        <div v-for="(kosentrasi, i) in kosentrasi" :key="i" class="card my-10">
          <div class="cardHead">
            <p class="text-[1.5rem]">{{ kosentrasi.name }}</p>
          </div>
          <div class="cardBody">
            <ol class="list-disc ms-5">
              <li v-for="list in kosentrasi.list" :key="list">{{ list }}</li>
            </ol>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
useHead ({ title: "Kejuruan - Kejuruan" })

import dkv from "../../assets/img/logodkv.png";
import rpl from "../../assets/img/pplg.png";
import tsm from "../../assets/img/tbsm.jpg";
import tkj from "../../assets/img/tjkt.png";
import toi from "../../assets/img/toi.jpg";

const logos = ref([
  { src: dkv, name: "Desain Komunikasi Visual" },
  { src: rpl, name: "Pengembangan Perangkat Lunak dan Gim" },
  { src: toi, name: "Teknik Elektronika" },
  { src: tkj, name: "Teknik Jaringan Komputer dan Telekomunikasi" },
  { src: tsm, name: "Teknik Otomotif" },
]);

const kosentrasi = ref([
  {
    name: "Pengembangan Perangkat Lunak dan Gim",
    list: ["Rekayasa Perangkat Lunak", "Pengembangan Gim"],
  },
  { name: "Desain Komunikasi Visual", 
    list: [""] },
  { name: "Teknik Elektronika", 
    list: [""] },
  { name: "Teknik Jaringan Komputer dan Telekomunikasi",
    list: [""] },
  { name: "Teknik Otomotif", 
    list: [""] },
]);
</script>

<style scoped></style>
