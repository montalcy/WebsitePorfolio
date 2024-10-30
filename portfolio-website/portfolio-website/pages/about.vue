<template>
  <v-row justify="center">
    <v-sheet
      class="pa-3 ma-3"
      style="width: fit-content; background-color: transparent"
      max-width="400"
      max-height="10"
    >
    </v-sheet>
  </v-row>

  <v-spacer></v-spacer>
  <v-row justify="center">
    <v-sheet
      class="pa-3 ma-3 animated-background"
      style="width: fit-content"
      border
      rounded
      :elevation="12"
      max-width="400"
    >
      <v-card-title class="text-center font" style="font-weight: bolder">
        Github <v-icon>mdi-github</v-icon>
      </v-card-title>
      <v-card-text class="font" style="text-align: center">
        This links to my github for you to see all the work I'm up to and have
        touched in the past!
      </v-card-text>
      <v-card-actions class="d-flex justify-center">
        <v-btn
          class="font"
          href="https://github.com/montalcy"
          target="_blank"
          variant="outlined"
          :elevation="9"
        >
          Github
        </v-btn>
      </v-card-actions>
    </v-sheet>

    <v-sheet
      class="pa-3 ma-3 animated-background"
      border
      rounded
      style="width: fit-content"
      :elevation="12"
      max-width="400"
    >
      <v-card-title class="text-center font" style="font-weight: bolder">
        LinkedIn <v-icon>mdi-linkedin</v-icon>
      </v-card-title>
      <v-card-text class="font" style="text-align: center">
        Wanna connect? <br />
        Check out my linked in by pressing the button down below!
      </v-card-text>
      <v-card-actions class="d-flex justify-center">
        <v-btn
          class="font"
          href="https://www.linkedin.com/in/cynthia-montalvo-792722302/"
          target="_blank"
          variant="outlined"
          :elevation="9"
        >
          LinkedIn
        </v-btn>
      </v-card-actions>
    </v-sheet>

    <v-sheet
      class="pa-3 ma-3 animated-background"
      border
      rounded
      style="width: fit-content"
      :elevation="12"
      max-width="400"
    >
      <v-card-title class="text-center font" style="font-weight: bolder">
        Flickr <v-icon>mdi-camera</v-icon>
      </v-card-title>
      <v-card-text class="font" style="text-align: center">
        Photography portfolio. I'd love for you to check out work I've done in
        the past!
      </v-card-text>
      <v-card-actions class="d-flex justify-center">
        <v-btn
          class="font"
          href="https://www.flickr.com/photos/197422998@N04/page1"
          target="_blank"
          variant="outlined"
          :elevation="9"
        >
          Flickr
        </v-btn>
      </v-card-actions>
    </v-sheet>
  </v-row>
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
