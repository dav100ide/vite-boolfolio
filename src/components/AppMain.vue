<template>
   <main>main</main>
</template>

<script>
import axios from 'axios';
export default {
   created() {
      axios
         .get('http://127.0.0.1:8000/api/projects') //
         .then((response) => {
            console.log(response.data);
         });
   },
};
</script>

<style lang="scss" scoped></style>
