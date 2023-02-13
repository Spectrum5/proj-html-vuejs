<script>
import AppTitle from "./components/AppTitle.vue"
import AppHero from "./components/AppHero.vue"

export default {
  components: {
    AppTitle,
    AppHero,
  },

  data() {
    return {
    }
  }
}
</script>

<template>
  <div class="container">
    <AppTitle />
    <AppHero />
  </div>
</template>

<style>

body {
  background-image: url('https://cdn.pixabay.com/photo/2012/08/25/22/22/saturn-54999_960_720.jpg');
  background-size: cover;
}

</style>