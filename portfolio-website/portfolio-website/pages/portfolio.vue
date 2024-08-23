<template>
  <v-container>
    <v-row>
      <v-col cols="3">
        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-card-title class="text-center font" style="font-weight: bolder">
            Github
          </v-card-title>
          <v-card-text class="font">
            This links to my github for you to see all the work I'm up to and
            have touched in the past!
          </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
              class="font"
              href="https://github.com/montalcy"
              target="_blank"
              variant="outlined"
            >
              Github
            </v-btn>
          </v-card-actions>
        </v-sheet>

        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-img src="/public/slotsOfFun.png"></v-img>
          <v-card-title class="text-center font" style="font-weight: bolder">
            Slots-Of-Fun!
          </v-card-title>
          <v-card-text class="font">
            This is a work in progress! This static web app is an attempt to
            simulate a slot machine. Although the front-end is the most
            progressed, I plan on making some more back end work to implement a
            real life database keeping track of users, coins and play frequency!
          </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
              class="font"
              href="https://www.linkedin.com/in/johannemcclenahan/"
              target="_blank"
              variant="outlined"
            >
              Play now
            </v-btn>
          </v-card-actions>
        </v-sheet>
      </v-col>

      <v-col cols="3" offset="1">
        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-card-title class="text-center font" style="font-weight: bolder">
          </v-card-title>
          <v-card-text class="font"> THIS IS UNDER CONSTRUCTION </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn> </v-btn>
          </v-card-actions>
        </v-sheet>

        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-card-title class="text-center font" style="font-weight: bolder">
          </v-card-title>
          <v-card-text class="font"> THIS IS UNDER CONSTRUCTION </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn> </v-btn>
          </v-card-actions>
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

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
