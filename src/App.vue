<template>
  <div id="app">
    <Header />
    <About />
    <Projects />
    <Skills />
    <footer class="container-fluid">
      <p class="float-end">
        <a href="#app" class="pe-5 pb-4 text-white">Back to Top</a>
      </p>
      <p class="text-white ps-5 pb-4">© Jiaxing 2022</p>
    </footer>
  </div>
</template>

<script>
import Header from "./views/Header";
import About from "./views/About";
import Projects from "./views/Projects";
import Skills from "./views/Skills";

export default {
  name: "App",
  components: {
    Header,
    About,
    Projects,
    Skills,
  },
  methods: {
    collapse() {
      document.getElementById("collapse-btn").click();
    },
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Josefin+Sans&display=swap");

* {
  max-width: 100%;
}

html,
body,
#app {
  height: 100%;
  scroll-behavior: smooth;
  max-width: 100%;
  font-family: "Josefin Sans", sans-serif;
}

footer {
  background-color: #313132;
}
</style>
