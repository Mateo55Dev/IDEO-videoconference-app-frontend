<script setup>
import './assets/styles/main.scss';
import { RouterView } from "vue-router"
import MainLayout from "./layouts/MainLayout.vue"
</script>

<template>
  <MainLayout>
      <RouterView></RouterView>
  </MainLayout>
</template>

