<template>
    <v-app-bar class="pa-2" :elevation="0">
        <template v-slot:prepend>
            <v-app-bar-title>Travel Tribe</v-app-bar-title>
        </template>
        <v-hover v-slot="{ isHovering, props }">
            <router-link to="/">
                <v-btn
                    icon="mdi-home"
                    alt="Home"
                    v-bind="props"
                    :color="isHovering ? 'purple' : 'black'"
                />
            </router-link>
        </v-hover>
        <v-hover v-for="(icon, index) in icons" :key="index" v-slot="{ isHovering, props }">
            <v-btn
                :icon="icon"
                class="ma-4"
                v-bind="props"
                :color="isHovering ? 'purple' : 'black'"
            />
        </v-hover>
        <template v-slot:append>
            <v-avatar color="surface-variant"></v-avatar>
        </template>
    </v-app-bar>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'

const icons = ['mdi-forum-outline', 'mdi-bell-outline', 'mdi-magnify']
</script>

<style scoped></style>

