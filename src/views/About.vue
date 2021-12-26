<template>
  <section id="about-section">
    <div class="container-fluid text-white pt-3" id="about">
      <div class="row justify-content-center text-center pt-3 m-0">
        <div
          class="col-md-6 col-sm-12 p-0"
          data-aos="flip-left"
          data-aos-duration="1000"
        >
          <img class="avatar" src="../assets/animated_avatar.gif" />
          <h1>About Me</h1>
          <p class="px-5">
            I love every single learning journey I embarked on through every
            project I partake. As a person that loves to learn by doing, I am
            always excited for new opportunities to expand my creativity,
            especially in the area of digital and technology product
            development.
          </p>
        </div>

        <div
          class="col-md-6 col-sm-12"
          data-aos="flip-right"
          data-aos-duration="1000"
        >
          <img class="contact" src="../assets/animated_contact.gif" />
          <h1>Contact</h1>

          <p>Email: jiaxing.yan.2022@gmail.com</p>
          <p>Languages: English, Chinese (Bilingual)</p>
          <a class="about-icons" href="https://t.me/kakyoyan">
            <i class="bi bi-telegram"></i>
          </a>
          <a class="about-icons" href="https://www.instagram.com/jiaxing_yz/">
            <i class="bi bi-instagram"></i>
          </a>
          <a class="about-icons" href="https://www.linkedin.com/in/jiaxingyan/">
            <i class="bi bi-linkedin"></i>
          </a>
          <a class="about-icons" href="https://github.com/jx-yan">
            <i class="bi bi-github"></i>
          </a>
        </div>
      </div>
    </div>
    <div class="spacer1"></div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
section#about-section {
  margin: 0%;
  background-color: #313132;
  height: auto;
}

.container-fluid {
  overflow-wrap: break-word;
}

img.contact {
  width: 200px;
  height: 173px;
}

img.avatar {
  width: 200px;
}

.bi {
  display: inline-block;
  font-size: 32px;
  color: #d1f3f9;
}

.about-icons {
  margin: 0px 1rem;
}

.about-transition {
  width: 100%;
  z-index: 0;
  object-fit: cover;
  max-height: 200px;
}

div.spacer1 {
  aspect-ratio: 960/300;
  width: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-image: url("../assets/wave-haikei.svg");
  height: 120px;
}
</style>
