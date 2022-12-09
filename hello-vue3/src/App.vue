<script setup lang="ts">
import {ref} from "vue";

const now = new Date().toLocaleTimeString();
const nowRef = ref(now);

const changeTime = () => {
  nowRef.value = new Date().toLocaleTimeString();
};

// 1秒ごとに実行
setInterval(changeTime, 1000);
</script>

<template>
  <div>
    <p>今の時刻: {{ nowRef }}</p>
  </div>
</template>
