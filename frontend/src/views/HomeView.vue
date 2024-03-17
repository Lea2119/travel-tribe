<template>
  <div class="pa-4">
    <CreatePost />
    <UserFeed />
    <DrawerRight />
    <DrawerLeft />
  </div>
</template>

<script setup lang="ts">
import UserFeed from '@/components/UserFeed.vue'
import CreatePost from '@/components/CreatePost.vue'
import DrawerRight from '@/components/DrawerRight.vue'
import DrawerLeft from '@/components/DrawerLeft.vue'
</script>

<style scoped></style>
