<script setup lang="ts">
import { ref } from "vue";

const message = ref("未送信です");
const onFormSubmit = () => {
  message.value = "送信されました";
};

</script>

<template>
  <div class="app">
    <form action="#" @submit.prevent="onFormSubmit">
      <input type="text" required />
      <button type="submit">送信</button>
    </form>
    <p>{{ message }}</p>
  </div>
</template>
