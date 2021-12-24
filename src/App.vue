<template>
  <div id="app">
    <nav class="navbar navbar-expand-sm fixed-top navbar-light p-0">
      <div class="container-fluid">
        <a class="navbar-brand" href="#home">
          <div class="logo-navbar"></div>
        </a>
        <button
          id="collapse-btn"
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNavAltMarkup"
          aria-controls="navbarNavAltMarkup"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse justify-content-end"
          id="navbarNavAltMarkup"
        >
          <ul class="navbar-nav text-center">
            <li class="nav-item">
              <a class="nav-link" href="#projects" @click="collapse"
                >Projects</a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#skills" @click="collapse">Skills</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
    <Header />
    <About />
    <Projects />
    <Skills />
    <footer class="container-fluid">
      <p class="float-end">
        <a href="#app" class="pe-5 pb-4 text-dark">Back to Top</a>
      </p>
      <p class="text-dark ps-5 pb-4">© Jiaxing 2022</p>
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

@media screen and (max-width: 575px) {
  .navbar-nav {
    background-color: aliceblue;
    border-radius: 10px;
  }
}

footer {
  background-color: #f8d5eb;
}
</style>
