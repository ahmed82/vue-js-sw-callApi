<template>
  <div class="Planets">
    <p>This is the Planets page</p>
    <ul>
      <li v-for="planet in planets" :key="planet.name">
        {{planet.name}}
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  name: 'Planets',
  async mounted() {
    const request = await fetch('https://swapi.dev/api/planets/');
    const { results } = await request.json();
    this.planets = results;
  },
  data() {
    return {
      planets: [],
    };
  },
};
</script>
