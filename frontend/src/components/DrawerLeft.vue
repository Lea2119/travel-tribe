<template>
  <v-navigation-drawer location="left" :width="300" class="drawer" floating>
    <v-list class="d-flex flex-column align-center justify-center mt-2">
      <div>
        <v-list-item class="d-flex flex-column text-center align-center justify-center mb-4">
          <v-avatar :image="avatar" size="100" class="mb-4" />
        </v-list-item>
        <v-card class="d-flex justify-center aligner-center text-center pa-2 mb-4">
          <v-list-item v-for="(value, title) in userStats" :key="title">
            <v-list-item-title class="font-weight-bold text-body-2">{{ value }}</v-list-item-title>
            <v-list-subtitle class="text-caption">{{ title }}</v-list-subtitle>
          </v-list-item>
        </v-card>
        <v-card>
          <v-list density="compact" nav>
            <v-list-item v-for="item in menuItems" :key="item.title">
              <template v-slot:prepend>
                <v-icon :icon="item.icon"></v-icon>
              </template>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-card>
      </div>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup lang="ts">
import avatar from '@/assets/user.jpg'

const userStats = {
  followers: 300,
  following: 300,
  events: 300
}

const menuItems = [
  { title: 'Feed', icon: 'mdi-home' },
  { title: 'Events', icon: 'mdi-calendar-week' },
  { title: 'Friends', icon: 'mdi-account-group' }
]
</script>

<style scoped>
.drawer {
  background-color: #f5f5f5;
}
</style>
