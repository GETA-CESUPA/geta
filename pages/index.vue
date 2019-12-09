<template>
  <div>
    <Introdution />
    <Info/>
    <Projects/>
  </div>
</template>

<script>
import Introdution from "~/components/Introdution.vue";
import Info from "~/components/Info.vue";
import Projects from '~/components/Projects.vue';

export default {
  components: {
    Introdution,
    Info,
    Projects
    
  }
};
</script>


