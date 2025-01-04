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
        <p class="text-[2.5rem] font-semibold">Guru dan Staff</p>
      </div>
    </div>
    <p class="paddingX">
      <NuxtLink to="/">Beranda</NuxtLink> /
      <span class="text-[#2c52b3]">Guru dan Staff</span>
    </p>
    <div class="paddingX my-7">
      <ul class="flex flex-wrap justify-center gap-5">
        <li v-for="teacher in teachers" :key="teacher.id">
          <div class="card">
            <div class="cardHead">
              <img :src="teacher.src" :alt="teacher.name" class="w-56" />
            </div>
            <div class="cardBody text-center">
              <p class="font-semibold">{{ teacher.name }}</p>
              <p class="text-[#11224eaa] text-[16px]">{{ teacher.subject }}</p>
            </div>
          </div>
        </li>
      </ul>
      <div class="flex justify-center gap-10 mt-5">
        <!-- {{ db_teachers.length }} -->
        <button
          v-if="teachers.length < db_teachers.length"
          @click="loadMore"
          class="bg-[#11224e] rounded-md py-2 px-4 text-white"
        >
          Lihat Lainnya
        </button>
        <button
          v-if="teachers.length > 5"
          @click="loadLess"
          class="bg-[#11224e] rounded-md py-2 px-4 text-white"
        >
          Lihat Sedikit
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import pp from "../../assets/img/gustaf/pp.jpeg";
import g1 from "../../assets/img/gustaf/1.jpeg";
import g2 from "../../assets/img/gustaf/2.jpeg";
import g3 from "../../assets/img/gustaf/3.jpeg";
import g4 from "../../assets/img/gustaf/4.jpeg";
import g5 from "../../assets/img/gustaf/5.jpeg";

const db_teachers = ref([
  {
    id: 1,
    src: g1,
    name: "Pak Arif",
    subject: "Kejuruan",
  },
  {
    id: 2,
    src: g2,
    name: "Bu Sri",
    subject: "IPAS",
  },
  {
    id: 3,
    src: g3,
    name: "Pak Deni",
    subject: "Kejuruan - PKK",
  },
  {
    id: 4,
    src: g4,
    name: "Pak Adi",
    subject: "Kejuruan",
  },
  {
    id: 5,
    src: g5,
    name: "Bu Lisna",
    subject: "Olahraga",
  },
  {
    id: 6,
    src: pp,
    name: "Jane Smith",
    subject: "Chemistry",
  },
  {
    id: 7,
    src: pp,
    name: "Smith John",
    subject: "Biology",
  },
  {
    id: 8,
    src: pp,
    name: "Smith Jane",
    subject: "Geography",
  },
  {
    id: 9,
    src: pp,
    name: "John Doe",
    subject: "Math",
  },
  {
    id: 10,
    src: pp,
    name: "Jane Doe",
    subject: "English",
  },
  {
    id: 11,
    src: pp,
    name: "Doe John",
    subject: "Science",
  },
  {
    id: 12,
    src: pp,
    name: "Doe Jane",
    subject: "History",
  },
  {
    id: 13,
    src: pp,
    name: "John Smith",
    subject: "Physics",
  },
  {
    id: 14,
    src: pp,
    name: "Jane Smith",
    subject: "Chemistry",
  },
  {
    id: 15,
    src: pp,
    name: "Smith John",
    subject: "Biology",
  },
  {
    id: 16,
    src: pp,
    name: "Smith Jane",
    subject: "Geography",
  },
  {
    id: 17,
    src: pp,
    name: "John Doe",
    subject: "Math",
  },
  {
    id: 18,
    src: pp,
    name: "Jane Doe",
    subject: "English",
  },
  {
    id: 19,
    src: pp,
    name: "Doe John",
    subject: "Science",
  },
  {
    id: 20,
    src: pp,
    name: "Doe Jane",
    subject: "History",
  },
  {
    id: 21,
    src: pp,
    name: "John Smith",
    subject: "Physics",
  },
  {
    id: 22,
    src: pp,
    name: "Jane Smith",
    subject: "Chemistry",
  },
  {
    id: 23,
    src: pp,
    name: "Smith John",
    subject: "Biology",
  },
  {
    id: 24,
    src: pp,
    name: "Smith Jane",
    subject: "Geography",
  },
  {
    id: 25,
    src: pp,
    name: "John Doe",
    subject: "Math",
  },
]);

// ambil 5 data teachers awal
const teachers = ref([...db_teachers.value.slice(0, 5)]);
const limitStart = ref(0); // batas awal pengambilan data
const limitEnd = ref(5); // batas akhir pengambilan data

// fungsi memuat data baru dari db_teachers
const loadMore = () => {
  // data lama di teachers digabung dengan 5 data dari db_teachers selanjutnya
  limitEnd.value += 5;
  teachers.value = [...db_teachers.value.slice(0, limitEnd.value)];

  // ubah limitStart dan limitEnd untuk data seterusnya
  limitStart.value = limitEnd.value - 5;
};

// fungsi memuat data baru dari db_teachers
const loadLess = () => {
  // data lama di teachers digabung dengan 5 data dari db_teachers sebelumnya
  if (limitStart.value >= 5) {
    // limitStart.value -= 5;
    limitEnd.value -= 5;
    teachers.value = [
      ...db_teachers.value.slice(0, limitEnd.value),
    ];
  }
};
</script>
