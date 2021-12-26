<template>
  <section id="projects">
    <p style="padding-bottom: 40px"></p>
    <div
      class="container-fluid text-center justify-content-center text-white p-0 m-0"
    >
      <h2 data-aos="zoom-in-down">My Projects</h2>
      <div class="timeline container-fluid p-0 m-0">
        <ul class="timeline-content pt-5">
          <TimelineItem
            v-for="(project, projectId, index) in projectItems"
            :key="index"
            :projectId="projectId"
            :project="project"
          ></TimelineItem>
        </ul>
      </div>
    </div>
    <div class="spacer2"></div>
  </section>
</template>

<script>
import TimelineItem from "./components/TimelineItem.vue";

export default {
  name: "Projects",
  components: {
    TimelineItem,
  },
  data() {
    return {
      projectItems: {
        item1: {
          timestamp: "Sep 2021 - Nov 2021",
          name: "Foodshare - Academic Project",
          imgUrl: "foodshare",
          description:
            "Foodshare is a web application that aims to tackle food wastage and scarcity in the UK. This is done through including 3 features, namely, Donate, Marketplace, and Knowledge, to raise awareness on food scarcity and to ease to process of donating and sharing food.",
          fileLink: "https://github.com/jx-yan/FoodShare",
          projectLink: "https://wad2-foodshare.web.app/",
          figmaLink: "",
          coverage: "",
        },
        item2: {
          timestamp: "Sep 2021 - Nov 2021",
          name: "HelpTogether - Academic Project",
          imgUrl: "",
          description:
            "HelpTogether is a mobile application that matches youths to suitable volunteering opportunities by taking into account their residential location, personalities and skills. Our application also streamlines the registration process of volunteering activities with an integrated platform that allows youths to connect and communicate with social organisations and other volunteers, and apply for volunteering activities with minimal hassle.",
          fileLink: "",
          projectLink:
            "https://www.figma.com/proto/BEF7I26WNRrHzFQaYyPaO5/G9T4-HelpTogether-Prototype?page-id=13780%3A14496&node-id=13924%3A19033&viewport=241%2C48%2C0.13&scaling=scale-down&starting-point-node-id=13924%3A19033&show-proto-sidebar=1",
          figmaLink: `<iframe width="100%" height="400px" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Ffile%2FBEF7I26WNRrHzFQaYyPaO5%2FG9T4-HelpTogether-Prototype%3Fnode-id%3D13780%253A14496" allowfullscreen></iframe>`,
          coverage: "",
        },
        item3: {
          timestamp: "Aug 2021 - Oct 2021",
          name: "Lit App - Financial Inclusion Hackathon 2021",
          imgUrl: "",
          description:
            "Lit App is an all-in-one financial management platform with 7 unique features such as automating expense tracking, providing daily budgeting that dynamically adjusts according to the user's spending pattern. The platform also incorporates social features such as virtual communities, financial goal syncing and an artificially intelligent chatbot that educate the user in terms of financial literacy. Achieved 1st Runner Up.",
          fileLink: "",
          projectLink:
            "https://www.figma.com/proto/lci46lnvgcijNNiQMYzNHX/Lit-App?page-id=0%3A1&node-id=53%3A157&viewport=241%2C48%2C0.06&scaling=scale-down&starting-point-node-id=120%3A2",
          figmaLink: `<iframe width="100%" height="400px" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Ffile%2Flci46lnvgcijNNiQMYzNHX%2FLit-App%3Fnode-id%3D0%253A1" allowfullscreen></iframe>`,
          coverage:
            "https://news.smu.edu.sg/news/2021/12/15/inaugural-financial-inclusion-hackathon-finhack-tackles-digital-financial-literacy",
        },
        item4: {
          timestamp: "Jun 2021 - Aug 2021",
          name: "Auxili - AWS Build On Asean 2021",
          imgUrl: "auxili",
          description:
            "Auxili is a platform that aims to improve the sharing landscape in Singapore, through a two pronged approach, with both a website and a telegram bot where it recommends the user a suitable volunteering service that takes in account of the geographical distance between the user, the social service's resource availability and the user's volunteering interest. Achieved 1st Runner Up.",
          fileLink: "",
          projectLink: "https://youtu.be/w9bL2K6V_WA",
          figmaLink: "",
          coverage:
            "https://www.linkedin.com/posts/sgsmuscis_buildonasean2021-aws-cognizant-activity-6828543210831314944-6rL4",
        },
      },
    };
  },
};
</script>

<style scoped>
section#projects {
  height: auto;
  width: 100%;
  margin: 0%;
  background-color: #002151;
}

h2 {
  display: flex;
  flex-direction: row;
}
h2:before,
h2:after {
  content: "";
  flex: 1 1;
  border-bottom: 3px solid;
  margin: auto;
}
h2:before {
  margin-right: 10px;
}
h2:after {
  margin-left: 10px;
}

div.spacer2 {
  aspect-ratio: 960/300;
  width: 100%;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  background-image: url("../assets/layered-peaks-haikei.svg");
  height: 160px;
}
</style>
