<template>
  <div class="home">
    <p>This is the Home page</p>
    <br>
      <router-link to="/planets">Planets</router-link>
    <br>
     <router-link to="/starships">Starships</router-link> <!-- Link the rout that match the path -->
    <router-view/>
  </div>
</template>
<script>
export default {
  name: 'Home',
};
</script>
