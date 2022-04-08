<template>
  <div id="app">
    <HeaderBar :header ="header"/>
    <FirstOjtContent :movies="moviesGet" />
    <FooterBar />
  </div>
</template>

<script>
import HeaderBar from './components/HeaderBar.vue'
import FirstOjtContent from './components/FirstOjtContent.vue'
import FooterBar from './components/FooterBar.vue'
import { mapGetters } from 'vuex'

export default {
  name: 'app',
  components: {HeaderBar, FirstOjtContent, FooterBar},
  data() {
    return {
      header: "Welcome From OJT project2",
    }
  },
  computed: {
    ...mapGetters(["movies"]),
    moviesGet() {
      return this.$store.getters.moviesNames;
    },
    moviesDirect() {
      return this.$store.state.movies;
    }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: 0;
  padding: 0;
  /* margin-top: 60px; */
}
body {
  margin: 0;
}
</style>
