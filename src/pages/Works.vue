<template>
  <q-page class="flex">
    <div class="q-pa-lg full-width text-bold">
      <div>
        <div class="hello text-h3 q-my-xl">Work Experience</div>
      </div>
      <div v-for="(work, index) in works" :key="index">
        <WorkCard :work="work" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import WorkCard from "components/WorkCard.vue";

export default defineComponent({
  name: "PageIndex",
  components: {
    WorkCard,
  },
  data() {
    return {
      works: [
        {
          establishment: {
            title: `Laboratório de Automação (LAUT)`,
            description: `The Automation Laboratory (LAUT) aims to house research in the field developed by UFRN in partnership with Petrobras and other companies.`,
            image: require("assets/logo_laut.png"),
          },
          work_description: `Worked on solutions intended to help engeneering companies to better manage its resources`,
          current: true,
        },
        {
          establishment: {
            title: `MED5`,
            description: `
              MED5 is a company that focus mainly on health related software solutions. The primary focus is an ecosystem that allows Doctors
               to better comunicate/manage their patients
            `,
            image: require("assets/med5-logo.png"),
          },
          work_description: `
            I worked on every aspect of this ecosystem, frontend with quasar/vueJS, backend with 
            Django rest api for the api and Node for a video conference module, and deploying with docker
            to the Amazon services
          `,
        },
        {
          establishment: {
            title: `Núcleo Avançado de Inovação Tecnológica (NAVI)`,
            description: `
              laboratory focused on the development of systems and technologies related to innovation
            `,
            image: require("assets/navi-logo.svg"),
          },
          work_description: `
            I worked on a project in the health sector, mainly backend development with PHP-Laravel, but also helped with some other tasks
          `,
        },
        {
          establishment: {
            title: `LAICA - Laboratório de Pesquisa Allyson Amilcar Angelus`,
            description: `
              LAICA's purpose is to conduct research and outreach in the areas of home automation,
               educational robotics, autonomous unmanned vehicles, and new information and communication technologies.
            `,
            image: require("assets/laica-logo.jpg"),
          },
          work_description: `
            I worked on a rubik's cube solving robot. It's main goal was to help with the teaching metodology relating to robotics on IFRN campuses. My work was related with arduino and hardware.
            This was also my first ever job
          `,
        },
      ],
    };
  },
});
</script>
<style scoped></style>
