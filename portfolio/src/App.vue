<template>
  <v-app>
    <div id="app">
      <img height="150px" width="150px" alt="Vue logo" src="./assets/profilepicture.jpg">
      <Main/>
    </div>
  <v-card
    height="200px">
    <v-footer padless>
      <v-card
        flat
        tile
        width="100%"
        class="blue lighten-1 text-center">
        <v-card-text>
          <v-btn
            v-for="icon in icons"
            :key="icon"
            class="mx-4"
            icon>
            <v-icon>{{ icon }}</v-icon>
          </v-btn>
        </v-card-text>
        
      </v-card>
    </v-footer>
  </v-card>
  </v-app>
</template>

<script>
import Main from './components/Main.vue'

export default {
  name: 'app',
  data() {
    return {
      icons: ['instagram', 'github', 'mail']
    }
  },
  components: {
    Main
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
