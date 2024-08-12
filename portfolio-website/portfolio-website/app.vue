<template>
  <NuxtLayout>
    <v-app class="animated-background">

      <v-app-bar >
          <v-list-item class="font"
            prepend-avatar="\cyndy.jpg"
            subtitle="2025 Graduate"
            title="Cynthia Montalvo"
          ></v-list-item>

          <v-spacer></v-spacer>
          
          <v-list-item density="compact" @click="router.push('/')">
            <v-list-item-icon>
              <v-icon >mdi-home-outline</v-icon>
            </v-list-item-icon>
          </v-list-item>
          <v-list-item density="compact" @click="router.push('/portfolio')">
            <v-list-item-icon>
              <v-icon> mdi-brain</v-icon>
            </v-list-item-icon>
          </v-list-item>
      </v-app-bar>
      
      <!-- Main content goes here -->
      <v-main>
      <v-container>
        <NuxtPage />
      </v-container>
    </v-main>
    </v-app>
  </NuxtLayout>
</template>

<script lang="ts" setup>
import { useRouter } from 'vue-router';
const router = useRouter();
</script>

<style scoped>
.animated-background {
  background: linear-gradient(45deg, #ff6b6b, #f7f7f7, #6bff6b);
  background-size: 600% 600%;
  animation: gradientAnimation 15s ease infinite;
  padding: 20px;
}

@keyframes gradientAnimation {
  0% { background-position: 0% 0%; }
  50% { background-position: 100% 100%; }
  100% { background-position: 0% 0%; }
}

/* Apply Roboto Light (300) to paragraphs */
.font {
  font-family:  monospace;
}

  </style>
