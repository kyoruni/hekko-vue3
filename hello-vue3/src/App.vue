<script setup lang="ts">
import {ref} from "vue";

const name = ref("hogehoge");
</script>

<template>
  <h1>こんにちは、{{ name }}！</h1>
</template>
