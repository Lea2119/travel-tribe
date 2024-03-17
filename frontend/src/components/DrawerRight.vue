<template>
  <v-navigation-drawer location="right" :width="300" class="drawer" floating>
    <v-list class="d-flex flex-column align-center justify-center mt-2">
      <div>
        <v-card>
          <v-list-item class="text-center mt-4">
            <v-list-item-title class="font-weight-bold">Suggestions</v-list-item-title>
            <v-list>
              <v-list-item
                prepend-avatar="https://cdn.vuetifyjs.com/images/john.png"
                title="John Leider"
              >
                <template v-slot:append>
                  <v-btn icon="mdi-account-plus" size="small" variant="text"></v-btn>
                </template>
              </v-list-item>
            </v-list>
          </v-list-item>
          <v-divider></v-divider>
        </v-card>
      </div>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup lang="ts"></script>

<style scoped>
.drawer {
  background-color: #f5f5f5;
}
</style>
