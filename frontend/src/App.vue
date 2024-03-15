<template>
  <v-layout>
      <AppBar />
      <RouterView />
  </v-layout>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppBar from './components/global/AppBar.vue'
</script>

<style scoped></style>

