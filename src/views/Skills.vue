<template>
  <section id="skills">
    <p style="padding-bottom: 40px"></p>
    <div class="container-fluid text-center justify-content-center">
      <div class="row skills-title pb-4" data-aos="fade-down">
        <h2>My Skills</h2>
        <hr class="my-0" />
      </div>
      <div class="row">
        <div
          class="col-lg-2 col-md-4 col-sm-6 py-4"
          v-for="(skill, name, index) in skills"
          :key="index"
          :skill="skill"
          :name="name"
          data-aos="flip-down"
        >
          <img
            :src="require('../assets/skill-logo/' + name + '-logo.png')"
            :alt="skill"
          />
          <h5 class="pt-3" v-html="skill"></h5>
        </div>
      </div>
    </div>
    <div class="spacer3"></div>
  </section>
</template>

<script>
export default {
  name: "Skills",
  data() {
    return {
      skills: {
        html: "HTML",
        css: "CSS",
        php: "PHP",
        js: "JavaScript",
        vuejs: "VueJS",
        reactjs: "ReactJS",
        nodejs: "NodeJS",
        python: "Python",
        git: "Git / Github",
        firebase: "Firebase",
        mysql: "SQL / MySQL",
        figma: "Figma",
      },
    };
  },
};
</script>

<style scoped>
section#skills {
  height: auto;
  width: 100%;
  margin: 0%;
  background-color: #f5c298;
}

hr {
  width: 10%;
  margin-left: auto;
  margin-right: auto;
  background-color: #333;
  border-top: 2px solid black;
  opacity: 1;
}

img {
  height: 145px;
}

div.spacer3 {
  aspect-ratio: 960/300;
  width: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-image: url("../assets/footer-layered-peak.svg");
  height: 130px;
}
</style>
