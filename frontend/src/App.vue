<template>
  <v-layout>
    <AppBar />
    <v-main>
      <RouterView />
    </v-main>
  </v-layout>
</template>

<script setup lang="ts">
import { RouterView } from 'vue-router'
import AppBar from '@/components/global/AppBar.vue'
</script>

<style scoped></style>
