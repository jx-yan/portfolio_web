<template>
  <header id="home">
    <Message />
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

<style>
header {
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
    url("../assets/ice_mountain.jpg");
  background-size: cover;
}

.logo-navbar {
  border-radius: 8px;
  max-height: 4.8rem;
  content: url("../assets/static_logo.png");
  cursor: default !important;
}

.logo-navbar:hover {
  content: url("../assets/animated_logo.gif");
  cursor: default !important;
  box-shadow: 1px 3px 5px rgba(0, 0, 0, 0.1);
}
</style>
