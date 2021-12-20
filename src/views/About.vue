<template>
  <section id="about">
    <div class="container-fluid mt-5">
      <div class="row justify-content-center text-center">
        <div class="col-6">
          <div class="row justify-content-center text-center mb-3">
            <img class="avatar" src="../assets/animated_avatar.gif" />
            <h1>About Me</h1>
          </div>
          <div class="row justify-content-center text-center">
            <div class="col-xl-8 col-lg-10 col-md-10 col-sm-12">
              <p>
                I love every single learning journey I embarked on through every
                project I partake. In my free time, I am always tinkering around
                with web development and learning about UX design. As an avid
                learner, I am always excited for new opportunities to expand my
                creativity, especially in the area of digital and technology
                product development.
              </p>
            </div>
          </div>
        </div>
        <div class="col-6 text-between">
          <div class="row justify-content-center text-center mb-3">
            <img class="contact" src="../assets/animated_contact.gif" />
            <h1>Contact</h1>
          </div>
          <div class="row justify-content-center text-center">
            <div class="col mb-3">
              <p>Email: jiaxing.yan.2022@gmail.com</p>
              <p>Languages: English, Chinese (Bilingual)</p>
              <a class="about-icons" href="#">
                <i class="bi bi-telegram"></i>
              </a>
              <a class="about-icons" href="#">
                <i class="bi bi-whatsapp"></i>
              </a>
              <a class="about-icons" href="#">
                <i class="bi bi-linkedin w"></i>
              </a>
              <a class="about-icons" href="#">
                <i class="bi bi-instagram"></i>
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "About",
};
</script>

<style scoped>
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
</style>
