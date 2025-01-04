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
        <p class="text-[2.5rem] font-semibold">Galeri</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Galeri</span>
    </p>
    <div class="paddingX">
        <div class="card shadow-md flex flex-col p-10 border-t rounded-2xl">
          <div class="cardHead text-center">
            <p class="text-[2rem] text-medium">Hari Kemerdekaan Indonesia Ke-79</p>
          </div>  
          <div class="cardBody flex flex-wrap justify-around gap-5">
            <img v-for="hut in hut" :key="hut" :src="hut.src" alt="Kegiatan Hari Kemerdekaan" class="w-96">
          </div>
        </div>
    </div>
    <div class="paddingX my-7">
        <div class="card shadow-md flex flex-col p-10 border-t rounded-2xl">
          <div class="cardHead text-center">
            <p class="text-[2rem] text-medium">Kegiatan PORSENI 2024</p>
          </div>  
          <div class="cardBody flex flex-wrap justify-around gap-5">
            <img v-for="porseni in porseni" :key="porseni" :src="porseni.src" alt="Kegiatan Hari Kemerdekaan" class="w-96">
          </div>
        </div>
    </div>
  </div>
</template>

<script setup>
useHead ({ title: "Galeri" })

import k1 from '../assets/img/galeri/k.jpeg'
import k2 from '../assets/img/galeri/k1.jpeg'
import k3 from '../assets/img/galeri/k2.jpeg'
import k4 from '../assets/img/galeri/k3.jpeg'
import k5 from '../assets/img/galeri/k4.jpeg'
import k6 from '../assets/img/galeri/k5.jpeg'
import p1 from '../assets/img/galeri/p1.jpeg'
import p2 from '../assets/img/galeri/p2.jpeg'
import p3 from '../assets/img/galeri/p3.jpg'
import p4 from '../assets/img/galeri/p4.jpeg'
// import p5 from '../assets/img/galeri/p5.jpeg'
import p6 from '../assets/img/galeri/p6.jpeg'

const hut = ref([
  {src: k1},
  {src: k2},
  {src: k3},
  {src: k4},
  {src: k5},
  {src: k6},
])

const porseni = ref([
  {src: p1},
  {src: p2},
  {src: p3},
  {src: p4},
  // {src: p5},
  {src: p6},
])
</script>

<style scoped></style>
