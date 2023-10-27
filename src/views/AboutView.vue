<template>
  <div>
    <p>Страница2</p>
    <button @click="show = !show">Начать</button>
    <pop-up v-if="show" @close="close" @submit="write"></pop-up>
  </div>
</template>
<script setup lang="ts">
import HelloWorld from "@/components/HelloWorld.vue";
import PopUp from "@/components/PopUp.vue";
import { Data } from "@/components/types";
import { ref } from "vue"; // @ is an alias to /src

const show = ref(false);
const write = (data: Data) => {
  console.log(data);
};
const close = () => {
  console.log("close");
};
</script>
