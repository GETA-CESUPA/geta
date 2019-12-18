<template>
  <div>
    <Introdution  />
    <Info id="info"/>
    <Projects id="projects"/>
    <Awards/>
    <Team />
    <Footer/>
  </div>
</template>

<script>
import Introdution from "~/components/Introdution.vue";
import Info from "~/components/Info.vue";
import Projects from '~/components/Projects.vue';
import Awards from '~/components/Awards.vue';
import Team from '~/components/Team.vue';

import Footer from '~/components/Footer.vue';

export default {
  components: {
    Introdution,
    Info,
    Projects,
    Awards,
    Footer,
    Team,
  }
};
</script>


