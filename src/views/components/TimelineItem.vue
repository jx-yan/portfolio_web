<template>
  <li class="timeline-card text-dark pb-5">
    <div class="container-fluid">
      <div class="row justify-content-end">
        <div
          class="timestamp col-3 text-white"
          v-html="project.timestamp"
          data-aos="fade-down"
          data-aos-duration="500"
        ></div>
        <div class="col-9" data-aos="fade-up" data-aos-duration="500">
          <div class="card justify-content-center">
            <img
              class="card-img-top"
              v-if="project.imgUrl == 'foodshare'"
              :src="require('../../assets/foodshare_static.png')"
            />
            <img
              class="card-img-top"
              v-if="project.imgUrl == 'auxili'"
              :src="require('../../assets/auxili.gif')"
            />
            <div
              class="figma card-img-top"
              v-else
              v-html="project.figmaLink"
            ></div>
            <div class="card-header">
              <h4 class="proj-title p-0 m-0" v-html="project.name"></h4>
            </div>
            <div class="card-body text-center">
              <p class="card-text" v-html="project.description"></p>
              <a
                v-if="project.projectLink !== ''"
                :href="project.projectLink"
                class="btn btn-info me-3 mb-2"
                >Demo</a
              >
              <a
                v-if="project.fileLink !== ''"
                :href="project.fileLink"
                class="btn btn-warning me-3 mb-2"
                >GitHub</a
              >
              <a
                v-if="project.coverage !== ''"
                :href="project.coverage"
                class="btn btn-warning me-3 mb-2"
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
