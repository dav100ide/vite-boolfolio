<template>
   <div>
      {{ project.name }}
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

<style lang="scss" scoped>
div {
   color: blueviolet;
}
</style>
