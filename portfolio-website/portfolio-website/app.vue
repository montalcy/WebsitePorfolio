<template>
  <NuxtLayout>
    <title>Cynthia Montalvo</title>
    <v-app class="animated-background">
      <v-app-bar>
        <v-list-item
          class="font"
          prepend-avatar="\cyndy.jpg"
          subtitle="2025 Graduate"
          title="Cynthia Montalvo"
        ></v-list-item>

        <v-spacer></v-spacer>
        
        <v-menu v-model="menu" offset-y v-if="isMobile" @click="menu = !menu">
          <template #activator="{ props }">
            <v-list-item v-bind="props">
              <v-icon>mdi-menu</v-icon>
            </v-list-item>
          </template>
          <v-list>
            <v-list-item color="white" class="font"  @click="router.push('/')">
              <v-list-item-title>Home <v-icon  size="x-small">mdi-home-outline</v-icon></v-list-item-title>
            </v-list-item>
            <v-list-item   class="font"  @click="router.push('/portfolio')">
              <v-list-item-title>Portfolio <v-icon size="x-small">mdi-brain</v-icon></v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-list v-else>
          <v-btn  variant="flat" class="font" @click="router.push('/portfolio')">
            <v-icon>mdi-brain</v-icon> Portfolio
          </v-btn>
          <v-btn variant="flat" class="font"  @click="router.push('/')">
          <v-list-item-icon>
            <v-icon size="large">mdi-home-outline</v-icon>
          </v-list-item-icon>
        </v-btn>
        </v-list>
        
        

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
import { useRouter } from "vue-router";
import { ref, onMounted, onBeforeUnmount } from 'vue';

const router = useRouter();
const menu = ref(false);
const isMobile = ref(false);
const checkWidth = () => {
  isMobile.value = window.innerWidth <= 600; 
};

onMounted(() => {
  checkWidth();
  window.addEventListener('resize', checkWidth);
});

onBeforeUnmount(() => {
  window.removeEventListener('resize', checkWidth);
});
</script>

<style scoped>
.animated-background {
  background: linear-gradient(45deg, #ff6b6b, #f7f7f7, #6bff6b);
  background-size: 600% 600%;
  animation: gradientAnimation 15s ease infinite;
  padding: 20px;
}

@keyframes gradientAnimation {
  0% {
    background-position: 0% 0%;
  }
  50% {
    background-position: 100% 100%;
  }
  100% {
    background-position: 0% 0%;
  }
}

.font {
  font-family: monospace;
}
</style>
