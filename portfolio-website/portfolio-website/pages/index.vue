<!-- THIS SECTION IS FOR MY ABOUT ME -->

<template>
  <v-card :elevation="12" height="650" class="rounded-class">
  <v-carousel
    :continuous="true"
    :show-arrows="false"
    height="650"
    delimiter-icon="mdi-checkbox-blank-circle"
    class="rounded-class"
  >
    <v-carousel-item height="700" class="animated-background">
      <br />
      <h1 style="text-align: center" class="font about-title">About me</h1>
      <br />
      <br />

      <h4 style="text-align: center" class="font about-text">Hello!👋</h4>
      <p style="text-align: center" class="font about-text">
        I'm a soon-to-be graduate with a degree in
        <strong>Computer Science </strong> from Eastern Washington University
        with both a minor in <br />
        <strong>Visual Communication Design </strong> and
        <strong>Spanish.</strong> <br />
        <br />
        Throughout my academic career, I've developed a strong foundation in API
        integration, problem solving, front and back end development, version
        control (git, github), testing, communication, and collaboration. For
        instance, during my internship at Spokane Teachers Credit Unit
        headquarters, I was able to work collaboratively with the team to create
        internal isolated function apps for STCU employees. This opportunity
        allowed me to work with languages such as C#, HTML and CSS allowing me
        to solidify my learning and grow my understanding of how front end and
        back end design work together. I'm particularly drawn to front end
        development because it allows you to think about how the consumer may
        benefit from your design options and allows me to put my design minor to
        use! Although I've enjoyed and have been able to grow my front end
        skills outside of school, I've had more experience with backend work and
        enjoy the process of problem solving through diverse problems. I'm eager
        to bring and grow my skills in a collaborative environment and
        contribute to a greater good!
        <br />
        <br />
        <strong>
          Check out some of my work by clicking the portfolio button above
        </strong>
        <br/>
        <br/>

       
      
      </p>
    </v-carousel-item>
    <v-carousel-item height="700" class="animated-background">
      <br />
      <h1 style="text-align: center" class="font about-title">Languages</h1>
      <br />
      <br />
      <p style="text-align: center" class="font about-text">
        
        <br />
        <h3>
          I have a solid foundation in backend development using:
        </h3>
        <strong>
          <br />
          <br />
          C# ⚙️
        </strong>
        - experience in object-oriented programming and .NET framework
        <br />

        <strong> Java☕ </strong>
        - developed applications and solutions to numerous projects throughout
        my education
        <strong>
          <br />
          SQL🗂️
        </strong>
        - basic understanding and experience with SQL for database querying and
        management
        <br />
        <br />
        <br />
        <h3>
          In addition to my backend experience, I am actively expanding my
          skills <br/>in front-end development using:
        </h3>
        <br />
        <br />

        <strong> HTML🖼️ </strong>
        -building and structuring web content
        <br />
        <strong> CSS🎨 </strong>
        -designing and styling visually appealing web interfaces
        <br />
      </p>
    </v-carousel-item>
    <v-carousel-item height="700" class="animated-background">
      <br />
      <h1 style="text-align: center" class="font about-title">Education</h1>
      <br />
      <br />


      <p style="text-align: center" class="font about-text">
        
        <br />
        <h3>
          Eastern Washington University
        </h3>
        <p>
          Cheney, Washington 99004
        </p>
       <br/>
       <br/>
        <h3>
          Major:
        </h3>
         Bachelor of Science in Computer Science🖥️
          <br/>
          <br/>
          <h3>
            Minors:
          </h3>
           Design, Spanish📚
           <br/>
           <br/>
          <h3>
          Graduation Date:
          </h3>
           Spring 2025🌻
          <br/>
          <br/>
          <h3>
          GPA:
          </h3>
          3.61
        </p>

    </v-carousel-item>
  </v-carousel>
</v-card>


</template>


<script setup>
import { useRouter } from "vue-router";
const router = useRouter();
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

.v-dialog {
  z-index: 1000; /* Adjust as necessary */
}

.rounded-class{
  border-radius: 20px;
}

@media (max-width: 768px) { 
  .about-text {
    font-family: monospace;
    font-size: .6rem;
  }

  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 375px) {
  .about-text {
    font-family: monospace;
    font-size: .5rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 820px) {
  .about-text {
    font-family: monospace;
    font-size: .9rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 540px) {
  .about-text {
    font-family: monospace;
    font-size: .7rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 344px) {
  .about-text {
    font-family: monospace;
    font-size: .5rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 412px) {
  .about-text {
    font-family: monospace;
    font-size: .6rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 320px) {
  .about-text {
    font-family: monospace;
    font-size: .5rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}

@media (max-width: 414px) {
  .about-text {
    font-family: monospace;
    font-size: .6rem;
  }
  .about-title {
    font-family: monospace;
    font-size: 1.0rem;
  }
}
</style>
