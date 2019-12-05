<template>
  <div id="app">
    <v-app id="inspire">
      <v-app-bar
        app
        clipped-left
      >
        <v-toolbar-title>Jack Wall</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn text>About</v-btn>
        <v-btn text>Education</v-btn>
        <v-btn text>Awards & Achievements</v-btn>
        <v-btn text>Skills & Projects</v-btn>
      </v-app-bar>
      <Home/>
      <v-footer app>
        <a><v-img src="@/assets/footer_icons/github-logo.svg" :aspect-ratio="16/9"></v-img></a>
      </v-footer>
    </v-app>
  </div>
</template>

<script>

import Home from '@/views/Home.vue'

export default {
  name: 'home',
  components: {
    Home
  }
}
</script>
