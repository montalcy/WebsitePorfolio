<!-- THIS SECTION IS FOR MY ABOUT ME -->

<template>
  <div class="animated-background">
    <h1 style="text-align: center" class="font">About me</h1>
    <br />
    <h4 style="text-align: center" class="font">Hello!👋</h4>
    <p style="text-align: center" class="font">
      I'm a soon-to-be graduate with a degree in
      <strong>Computer Science </strong> from Eastern Washington University with
      both a minor in <br />
      <strong>Visual Communication Design </strong> and
      <strong>Spanish.</strong> <br />
      <br />

      Throughout my academic career, I've developed a strong foundation in API
      integration, problem solving, front and back end development, version
      control (git, github), testing, communication, and collaboration. For
      instance, during my internship at Spokane Teachers Credit Unit
      headquarters, I was able to work collaboratively with the team to create
      internal isolated function apps for STCU employees. This opportunity
      allowed me to work with languages such as C#, HTML and CSS allowing me to
      solidify my learning and grow my understanding of how front end and back
      end design work together. I'm particularly drawn to front end development
      because it allows you to think about how the consumer may benefit from
      your design options and allows me to put my design minor to use! Although
      I've enjoyed and have been able to grow my front end skills outside of
      school, I've had more experience with backend work and enjoy the process
      of problem solving through diverse problems. I'm eager to bring and grow
      my skills in a collaborative environment and contribute to a greater good!
      <br />
      <br />
      <strong>
        Check out some of my work by clicking the brain icon up at the top 🧠
      </strong>
      <br />
      <br />
      <strong>Languages: </strong>
      <br />
      C#
      <br />
      HTML
      <br />
      CSS
      <br />
      Java
      <br />
      SQL
      <br />
    </p>
  </div>

  <!-- THIS SECTION IS FOR THE POPUP -->

  <v-dialog width="500">
    <template v-slot:activator="{ props: activatorProps }">
      <v-container>
        <v-row justify="center">
          <v-col class="text-center">
            <v-btn
              v-bind="activatorProps"
              color="white"
              text
              variant="elevated"
              class="font"
            >
              <v-icon>mdi-human-greeting-proximity</v-icon>
              CONTACT ME
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </template>

    <template v-slot:default="{ isActive }">
      <v-card-text>
        <v-card-text
          style="text-align: center; font-size: large"
          class="pd"
          height="10"
        >
          <!-- THIS SECTION IS FOR THE POPUP CLOSE CIRCLE -->

          <v-alert class="animated-background">
            <v-card-actions>
              <v-btn
                color="black"
                density="compact"
                icon="mdi-close-circle-outline"
                @click="isActive.value = false"
              />
            </v-card-actions>

            <!-- THIS SECTION IS FOR THE POPUP CONTENT -->

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
      </v-card-text>

      <v-card-actions>
        <v-spacer></v-spacer>
      </v-card-actions>
    </template>
  </v-dialog>

  <!-- THIS SECTION IS FOR THE FOOTER AT BOTTOM OF PAGE -->

  <footer class="footer">
    <p class="font">
      <br />
      <br />
      &copy; My Portfolio Website 2024
    </p>
  </footer>
</template>

<script setup>
const email = "cynthia.1.montalvo@gmail.com";
const phone = "(509) 200-8939";
const linkedinUrl = "https://www.linkedin.com/in/cynthia-montalvo-792722302";
const githubUrl = "https://github.com/montalcy";
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
.footer {
  text-align: center;
  margin: 20px 0;
  font-family: "Roboto", sans-serif;
  font-weight: 300;
}
</style>
