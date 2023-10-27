<template>
  <div id="popupWrapper" @click.self="close">
    <div id="popup" style="max-width: 500px">
      <h3>Заголовок попапа</h3>
      <div class="input-container">
        <input v-model="data.data1" type="text" placeholder="Поле 1" />
        <input v-model="data.data2" type="text" placeholder="Поле 2" />
      </div>
      <div class="input-container">
        <input v-model="data.data3" type="text" placeholder="Поле 3" />
        <input v-model="data.data4" type="text" placeholder="Поле 4" />
      </div>
      <div class="input-container">
        <input v-model="data.data5" type="text" placeholder="Поле 5" />
      </div>
      <button @click="submitForm">Отправить</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineEmits, ref } from "vue";
import { Data } from "@/components/types";

const fileds = ref([]);
const data = ref({
  data1: "",
  data2: "",
  data3: "",
  data4: "",
  data5: "",
});
const emit = defineEmits<{
  (event: "submit", data: Data): Data;
  (event: "close"): void;
}>();
const close = () => {
  emit("close");
};
const submitForm = () => {
  emit("submit", data.value);
};
</script>

<style scoped></style>
