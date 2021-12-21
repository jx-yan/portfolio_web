<template>
  <section id="projects">
    <p style="padding-bottom: 100px"></p>
    <div class="container-fluid text-center text-white justify-content-center">
      <h1 data-aos="zoom-in-down">My Projects</h1>
    </div>
  </section>
</template>

<script>
export default {
  name: "Projects",
};
</script>

<style scoped>
section#projects {
  height: 100%;
  width: 100%;
  margin: 0%;
  background-color: #0066ff;
}

h1 {
  display: flex;
  flex-direction: row;
}
h1:before,
h1:after {
  content: "";
  flex: 1 1;
  border-bottom: 3px solid;
  margin: auto;
}
h1:before {
  margin-right: 10px;
}
h1:after {
  margin-left: 10px;
}
</style>
