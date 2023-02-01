<template>
   <main class="container-fluid">
      <div class="row g-3">
         <ProjectCard v-for="project in projects" :project="project" />
      </div>
   </main>
</template>

<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';

export default {
   components: {
      ProjectCard,
   },

   data() {
      return {
         projects: [],
      };
   },
   created() {
      axios
         .get('http://127.0.0.1:8000/api/projects') //
         .then((response) => {
            console.log(response.data[0]);
            this.projects = response.data;
         });
   },
};
</script>

<style lang="scss" scoped></style>
