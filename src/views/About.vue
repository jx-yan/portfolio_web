<template>
  <section id="about-section">
    <div class="container-fluid mt-5" id="about">
      <div class="row justify-content-center text-center">
        <div class="col-6" data-aos="fade-right" data-aos-duration="1000">
          <div class="row justify-content-center text-center mb-3">
            <img class="avatar" src="../assets/animated_avatar.gif" />
            <h1>About Me</h1>
          </div>
          <div class="row justify-content-center text-center">
            <div class="col-xl-8 col-lg-10 col-md-10 col-sm-12">
              <p>
                I love every single learning journey I embarked on through every
                project I partake. As a person that loves to learn by doing, I
                am always excited for new opportunities to expand my creativity,
                especially in the area of digital and technology product
                development.
              </p>
            </div>
          </div>
        </div>
        <div class="col-6" data-aos="fade-left" data-aos-duration="1000">
          <div class="row justify-content-center text-center mb-3">
            <img class="contact" src="../assets/animated_contact.gif" />
            <h1>Contact</h1>
          </div>
          <div class="row justify-content-center text-center">
            <div class="col mb-3">
              <p>Email: jiaxing.yan.2022@gmail.com</p>
              <p>Languages: English, Chinese (Bilingual)</p>
              <a class="about-icons" href="https://t.me/kakyoyan">
                <i class="bi bi-telegram"></i>
              </a>
              <a
                class="about-icons"
                href="https://www.instagram.com/jiaxing_yz/"
              >
                <i class="bi bi-instagram"></i>
              </a>
              <a
                class="about-icons"
                href="https://www.linkedin.com/in/jiaxingyan/"
              >
                <i class="bi bi-linkedin"></i>
              </a>
              <a class="about-icons" href="https://github.com/jx-yan">
                <i class="bi bi-github"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <img class="about-transition p-0" src="../assets/layered-waves.svg" />
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
}

.about-icons {
  margin: 0px 1rem;
}

.about-transition {
  width: 100%;
  z-index: 0;
  object-fit: cover;
  max-height: 300px;
}
</style>
