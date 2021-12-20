<template>
  <div id="app">
    <Header />
    <About />
    <Projects />
    <Skills />
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
};
</script>

<style>
html,
body,
#app {
  height: 100%;
  scroll-behavior: smooth;
  font-family: "Inter", sans-serif;
}

nav {
  display: block;
}

a .navbar-brand {
  cursor: default !important;
}

.logo-navbar {
  border-radius: 8px;
  max-height: 5rem;
  content: url("./assets/static_logo.png");
  cursor: default !important;
}

.logo-navbar:hover {
  content: url("./assets/animated_logo.gif");
  cursor: default !important;
  box-shadow: 1px 3px 5px rgba(0, 0, 0, 0.1);
}

.navbar-nav .nav-link {
  color: #000000;
  margin-left: 2rem;
  margin-right: 2rem;
  border-radius: 10px;
  font-weight: 500;
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}

.navbar-light .navbar-nav .nav-link.active {
  color: #000000 !important;
  background-color: white !important;
  box-shadow: 1px 3px 5px rgba(0, 0, 0, 0.1);
  opacity: 80%;
}

.navbar-nav .nav-link:hover {
  color: #000000 !important;
  background-color: white !important;
  box-shadow: 1px 3px 5px rgba(0, 0, 0, 0.1);
  opacity: 80%;
}

.navbar-toggler-icon {
  color: #545454;
}

header {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  height: 100%;
  width: 100%;
  background: no-repeat center center fixed;
  background-image: linear-gradient(
      to right bottom,
      rgba(34, 34, 34, 0.2),
      rgba(34, 34, 34, 0.2)
    ),
    url("./assets/ice_mountain.jpg");
  background-size: cover;
}

@media screen and (max-width: 992px) {
  .navbar-nav {
    background-color: aliceblue;
    border-radius: 10px;
  }
}
</style>
