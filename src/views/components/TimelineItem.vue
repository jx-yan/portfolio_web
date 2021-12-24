<template>
  <li class="timeline-card text-dark pb-5">
    <div class="container-fluid">
      <div class="row justify-content-end">
        <div
          class="col-3 text-white"
          v-html="project.timestamp"
          data-aos="fade-right"
        ></div>
        <div class="col-9" data-aos="fade-up-left">
          <div class="card justify-content-center">
            <img
              class="card-img-top"
              v-if="project.imgUrl == 'foodshare'"
              :src="require('../../assets/foodshare_static.png')"
            />
            <div class="card-header">
              <h4 class="p-0 m-0" v-html="project.name"></h4>
            </div>
            <div class="card-body">
              <div class="figma" v-html="project.figmaLink"></div>
              <p class="card-text" v-html="project.description"></p>
              <a
                v-if="project.projectLink !== ''"
                :href="project.projectLink"
                class="btn btn-info me-3"
                >Demo</a
              >
              <a
                v-if="project.fileLink !== ''"
                :href="project.fileLink"
                class="btn btn-warning me-3"
                >GitHub</a
              >
              <a
                v-if="project.coverage !== ''"
                :href="project.coverage"
                class="btn btn-warning me-3"
                >Coverage</a
              >
            </div>
          </div>
        </div>
      </div>
    </div>
  </li>
</template>

<script>
export default {
  name: "TimelineItem",
  props: ["key", "projectId", "project"],
  data() {
    return {
      imgUrl: this.project.imgUrl,
    };
  },
};
</script>

<style scoped>
li.timeline-card {
  list-style-type: none;
}
</style>
