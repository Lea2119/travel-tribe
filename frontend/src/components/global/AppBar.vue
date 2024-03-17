<template>
  <v-app-bar>
    <template v-slot:prepend>
      <v-app-bar-title>Travel Tribe</v-app-bar-title>
    </template>
    <v-btn v-for="icon in icons" :key="icon.index">
      <v-icon size="large">{{ icon }}</v-icon>
    </v-btn>
    <template v-slot:append>
      <v-menu>
        <template v-slot:activator="{ props }">
          <v-btn icon v-bind="props">
            <v-avatar :image="avatar" tile size="large" class="rounded" />
          </v-btn>
        </template>
        <v-card>
          <v-card-text>
            <div class="mx-auto text-center">
              <v-btn variant="text" rounded> Create Post </v-btn>
              <v-divider class="my-3"></v-divider>
              <v-btn variant="text" rounded> Create Event </v-btn>
              <v-divider class="my-3"></v-divider>
              <v-btn variant="text" rounded> Edit Account </v-btn>
              <v-divider class="my-3"></v-divider>
              <v-btn variant="text" rounded> Disconnect </v-btn>
            </div>
          </v-card-text>
        </v-card>
      </v-menu>
    </template>
  </v-app-bar>
</template>

<script setup lang="ts">
import avatar from '@/assets/user.jpg'

const icons = ['mdi-forum-outline', 'mdi-bell-outline', 'mdi-magnify']
</script>

<style scoped></style>