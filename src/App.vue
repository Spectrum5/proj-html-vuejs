<script>
import { store } from './store.js';
import AppHeader from "./components/Header/AppHeader.vue"
import AppMain from "./components/Main/AppMain.vue"
import AppFooter from "./components/Footer/AppFooter.vue"

export default {
  name: "App",
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },

  data() {
    return {
      store,
    }
  },

  methods: {
  }
}
</script>

<template>
    <AppHeader />
    <AppMain />
    <AppFooter />
</template>

<style lang="scss">
@use "./styles/main.scss" as *;
</style>