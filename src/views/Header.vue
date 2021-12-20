<template>
  <header id="home">
    <a name="myanchor">
      <h1
        style="padding-top: 40px; margin-top: -40px; padding-bottom: 100px"
      ></h1>
    </a>
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

<style></style>
