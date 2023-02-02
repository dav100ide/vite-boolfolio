<template>
   <div class="col-6 col-md-3">
      <div class="card h-100">
         <img
            v-if="project.cover_image"
            :src="project.cover_image"
            :alt="project.name"
            class="card-img-top"
         />
         <img v-else src="https://via.placeholder.com/150" alt="placeholder" />
         <div class="card-body">
            <h5 class="card-title">
               {{ project.name }}
            </h5>
            <p class="card-text">
               {{ project.description }}
            </p>
         </div>
      </div>
   </div>
</template>

<script>
export default {
   props: {
      project: {
         type: Object,
         default: {
            id: null,
            name: 'nome di default',
            slug: 'slug-di-default',
            description: 'descrizione di default',
            cover_image: null,
            customer: 'customer di default',
            created_at: null,
            updated_at: null,
            image_url: null,
            technologies: [],
         },
      },
   },
};
</script>

<style lang="scss" scoped></style>
