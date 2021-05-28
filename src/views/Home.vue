<template>
  <div class="home">
    <p>This is the Home page</p>
    <br>
    <div v-show="isHome">
        <router-link to="/planets" tag="button">Planets</router-link>
      <br><br>
        <router-link to="/starships" tag="button">Starships</router-link>
        <!-- Link the rout that match the path -->
     </div>
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'Home',
  computed: {
    isHome() {
      return this.$route.name === 'Home';
    },
  },
};
</script>
