<template>
  <v-container>
    <v-row>
      <v-col cols="3">
        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-card-title class="text-center font" style="font-weight: bolder">
            Github <v-icon>mdi-github</v-icon>
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
              href="https://black-water-0a7392b1e.5.azurestaticapps.net/"
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
            LinkedIn<v-icon>mdi-linkedin</v-icon>
          </v-card-title>
          <v-card-text class="font">
            Wanna connect? Check out my linked in by pressing the button down below!
          </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
              class="font"
              href="https://www.linkedin.com/in/cynthia-montalvo-792722302/"
              target="_blank"
              variant="outlined"
            >
              LinkedIn
            </v-btn>
          </v-card-actions>
        </v-sheet>

        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
        <v-img src="/public/wordle1.png"></v-img>
          <v-card-title class="text-center font" style="font-weight: bolder">
            HillBiddle!
          </v-card-title>
          <v-card-text class="font"> Class project where we recreated the game Wordle! My partner and I were challenged with working with full-stack development.
            Unfortunately, it hasn't been correctly set up with our database (I plan to
            take this project up again and re-vamp it)! </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
            class="font"
              href="https://gentle-sand-0aaa3be10.5.azurestaticapps.net/"
              target="_blank"
              variant="outlined"
            > Play now </v-btn>
          </v-card-actions>
        </v-sheet>
      </v-col>

      <v-col cols="3" offset="1">
        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
          <v-card-title class="text-center font" style="font-weight: bolder">
            Flickr <v-icon>mdi-camera</v-icon>
          </v-card-title>
          <v-card-text class="font">
            Photography portfolio. I'd love for you
            to check out other work I've done in the past! 
          </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
              class="font"
              href="https://www.flickr.com/photos/197422998@N04/page1"
              target="_blank"
              variant="outlined"
            >
              Flickr
            </v-btn>
          </v-card-actions>
        </v-sheet>

        <v-sheet
          class="pa-3 ma-3 animated-background"
          style="width: fit-content"
        >
        <v-img src="/public/guess.png"></v-img>
          <v-card-title class="text-center font" style="font-weight: bolder">
            Guess the billy!
          </v-card-title>
          <v-card-text class="font"> My first class project where we had the task to create a simple
            static web app with only front-end work and deploy it to azure. We decided on a simple guessing game.
            This is the beginning of the HillBilly saga. It was also my first time touching front-end development.
          </v-card-text>
          <v-card-actions class="d-flex justify-center">
            <v-btn
            class="font"
              href="https://mango-tree-002df5010.5.azurestaticapps.net/"
              target="_blank"
              variant="outlined"
            > Play now </v-btn>
          </v-card-actions>
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
  <footer class="footer" style="text-align: center">
    <p class="font">&copy; My Portfolio Website 2024</p>
  </footer>
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
