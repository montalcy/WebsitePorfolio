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
            <v-list-item color="white" class="font" @click="router.push('/')">
              <v-list-item-title>Home </v-list-item-title>
            </v-list-item>
            <v-list-item class="font" @click="router.push('/portfolio')">
              <v-list-item-title>Portfolio </v-list-item-title>
            </v-list-item>
            <v-list-item class="font" @click="router.push('/about')">
              <v-list-item-title>Connect </v-list-item-title>
            </v-list-item>
          </v-list>
        </v-menu>

        <v-list v-else>
          <v-btn
            size="small"
            variant="flat"
            class="font"
            @click="router.push('/')"
          >
            <v-list-item-icon>
              <v-icon>mdi-home-outline</v-icon>
            </v-list-item-icon>
          </v-btn>
          <v-btn
            size="small"
            variant="flat"
            class="font"
            @click="router.push('/portfolio')"
          >
            Portfolio
          </v-btn>
          <v-btn
            size="small"
            variant="flat"
            class="font"
            @click="router.push('/about')"
          >
            Connect
          </v-btn>
        </v-list>
      </v-app-bar>

      <!-- Main content goes here -->
      <v-main>
        <v-container>
          <NuxtPage />

          <v-dialog width="500">
            <template v-slot:activator="{ props: activatorProps }">
              <v-container style="padding-top: 29px">
                    <v-btn
                    
                      v-bind="activatorProps"
                      color="white"
                      variant="elevated"
                      class="font"
                      icon="$vuetify"
                      :elevation="12"
                      style="font-size: small; position: fixed; 
                bottom: 20px; 
              right: 20px; 
                     z-index: 1000;"

                    >
                     <v-icon>mdi-human-greeting-proximity</v-icon>

                    </v-btn>
              </v-container>
            </template>

            <template v-slot:default="{ isActive }">
              <v-card-text>
                <v-card-text
                  style="text-align: center; font-size: large"
                  class="pd"
                  rounded
                  border
                  height="10"
                >
                  <!-- THIS SECTION IS FOR THE POPUP CLOSE CIRCLE -->
                  <v-alert class="animated-background" style="padding-bottom: 20%;">
                    <!-- THIS SECTION IS FOR THE POPUP CONTENT -->
                    <v-list-item-icon>
                      <v-card-actions>
                        <v-btn 
                          color="black"
                          density="compact"
                          icon="mdi-close-outline"
                          @click="isActive.value = false"
                          style=" 
                       z-index: 1000;"
                        />
                      </v-card-actions>
                      <v-icon>mdi-email-heart-outline</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      <v-list-item-title class="font">Email:</v-list-item-title>
                      <v-list-item-subtitle class="font">
                        <a :href="'mailto:' + email">{{ email }}</a>
                      </v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-icon>
                      <v-icon>mdi-phone</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      <v-list-item-title class="font">Phone:</v-list-item-title>
                      <v-list-item-subtitle class="font">
                        <a :href="'tel:' + phone">{{ phone }}</a>
                      </v-list-item-subtitle>
                    </v-list-item-content>

                    <v-icon>mdi-linkedin</v-icon>
                    <v-list-item-content>
                      <v-list-item-title class="font"
                        >LinkedIn:</v-list-item-title
                      >
                      <v-list-item-subtitle class="font">
                        <a
                          :href="linkedinUrl"
                          target="_blank"
                          rel="noopener noreferrer"
                          >{{ linkedinUrl }}</a
                        >
                      </v-list-item-subtitle>
                    </v-list-item-content>

                    <v-list-item-icon>
                      <v-icon>mdi-github</v-icon>
                    </v-list-item-icon>
                    <v-list-item-content>
                      <v-list-item-title class="font"
                        >Github:</v-list-item-title
                      >
                      <v-list-item-subtitle class="font">
                        <a
                          :href="githubUrl"
                          target="_blank"
                          rel="noopener noreferrer"
                          >{{ githubUrl }}</a
                        >
                      </v-list-item-subtitle>
                    </v-list-item-content>
                  </v-alert>
                </v-card-text>
                <v-divider />
              </v-card-text>

              <v-card-actions>
                <v-spacer></v-spacer>
              </v-card-actions>
            </template>
          </v-dialog>
          <!-- THIS SECTION IS FOR THE FOOTER AT BOTTOM OF PAGE -->
          <footer class="footer">
            <p class="font">
              &copy; 2024 Cynthia Montalvo. All rights reserved.
            </p>
          </footer>
        </v-container>
      </v-main>
    </v-app>
  </NuxtLayout>
</template>

<script lang="ts" setup>
import { useRouter } from "vue-router";
import { ref, onMounted, onBeforeUnmount } from "vue";

const router = useRouter();
const menu = ref(false);
const isMobile = ref(false);
const email = "cynthia.1.montalvo@gmail.com";
const phone = "(509) 200-8939";
const linkedinUrl = "https://www.linkedin.com/in/cynthia-montalvo-792722302";
const githubUrl = "https://github.com/montalcy";
const checkWidth = () => {
  isMobile.value = window.innerWidth <= 600;
};

onMounted(() => {
  checkWidth();
  window.addEventListener("resize", checkWidth);
});

onBeforeUnmount(() => {
  window.removeEventListener("resize", checkWidth);
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

.footer {
  padding-top: 8px;
  text-align: center;
  margin: 20px 0;
  font-family: "Roboto", sans-serif;
  font-weight: 300;
}
.font {
  font-family: monospace;
}
</style>
