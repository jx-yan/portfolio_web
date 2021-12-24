<template>
  <header id="home">
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
    <h1
      style="padding-top: 40px; margin-top: -40px; padding-bottom: 100px"
    ></h1>
    <Message class="animate__animated animate__backInLeft" />
  </header>
</template>

<script>
import Message from "./components/Message.vue";
export default {
  name: "Header",
  components: {
    Message,
  },
};
</script>

<style scoped>
nav {
  display: block;
}

a .navbar-brand {
  cursor: default !important;
}

.logo-navbar {
  border-radius: 8px;
  max-height: 5rem;
  content: url("../assets/static_logo.png");
  cursor: default !important;
}

.logo-navbar:hover {
  content: url("../assets/animated_logo.gif");
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

.navbar-toggler-icon {
  color: #545454;
}

@media screen and (max-width: 575px) {
  .navbar-nav {
    background-color: aliceblue;
    border-radius: 10px;
  }
}
</style>
