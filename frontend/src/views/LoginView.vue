<template>
  <div class="d-flex ma-4">
    <v-card title="Login" class="pa-4 ma-4 w-50">
      <v-card-text>
        Welcome back to Travel Tribe! We're excited to help you plan your next adventure. Log in to
        connect with fellow travelers, share your experiences, and discover new destinations. Let's
        explore the world together!
      </v-card-text>
      <v-card-text class="font-weight-bold">
        Don't have an account?<router-link
          to="/register"
          class="text-decoration-underline font-weight-bold"
          >Click here</router-link
        >to create one
      </v-card-text>
    </v-card>
    <v-card class="pa-4 ma-4 w-50">
      <v-form class="pa-4">
        <v-text-field label="Email" variant="outlined" class="ga-2"></v-text-field>
        <v-text-field
          label="Password"
          variant="outlined"
          :append-inner-icon="visible ? 'mdi-eye' : 'mdi-eye-off'"
          :type="visible ? 'text' : 'password'"
          @click:append-inner="visible = !visible"
          class="ga-2"
        ></v-text-field>
        <v-btn type="submit" block color="purple" variant="flat">Submit</v-btn>
      </v-form>
    </v-card>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const visible = ref(false)
</script>

<style scoped></style>
