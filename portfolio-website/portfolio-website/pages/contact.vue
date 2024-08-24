<template>
  <Transition name="modal">
    <v-dialog v-model="modelValue" width="500">
      <v-card>
        <v-card-text
          style="text-align: center; font-size: large"
          class="pd"
          height="10"
        >
          <v-card-actions>
            <v-btn
              color="black"
              density="compact"
              icon="mdi-close-circle-outline"
              @click="modelValue = false"
            />
          </v-card-actions>

          <v-alert class="animated-background">
            <v-list-item-icon>
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
              <v-list-item-title class="font">LinkedIn:</v-list-item-title>
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
              <v-list-item-title class="font">Github:</v-list-item-title>
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
      </v-card>
    </v-dialog>
  </Transition>
</template>

<script lang="ts" setup>
import { ref } from "vue";
import { useRouter } from "vue-router";

const router = useRouter();
function toggleDialog() {
  modelValue.value = !modelValue.value;
}
const email = "cynthia.1.montalvo@gmail.com";
const phone = "(509) 200-8939";
const linkedinUrl = "https://www.linkedin.com/in/cynthia-montalvo-792722302/";
const githubUrl = "https://github.com/montalcy";

const modelValue = ref(true);
</script>

<style>
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
.pd {
  font-family: monospace;
}

.custom-card {
  max-width: 600px;
  margin: auto;
  padding: 20px;
}

.centered-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
</style>
