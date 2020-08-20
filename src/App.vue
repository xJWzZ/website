<template>
  <div id="app">
    <v-app id="inspire">
      <v-app-bar
        app
        clipped-left
      >
        <v-toolbar-title>Jack Wall</v-toolbar-title>
        <v-spacer></v-spacer>
        <div v-for='link in links' :key='link.text' class='ma-1'>
          <v-btn text router :to='link.route'>
            <v-icon class="mr-1">mdi-{{link.icon}}</v-icon>
            {{link.text}}
          </v-btn>
        </div>
      </v-app-bar>
      <v-content>
        <router-view/>
      </v-content>
    </v-app>
  </div>
</template>

<script>

export default {
  data () {
    return {
      links: [
        { text: 'Home', route: '/', icon: 'home-outline' },
        { text: 'Work', route: '/work-experience', icon: 'briefcase' },
        { text: 'Education', route: '/education', icon: 'school' },
        { text: 'Awards & Achievements', route: '/awards', icon: 'trophy-award' },
        { text: 'Skills & Projects', route: '/skills', icon: 'projector-screen' }
      ]
    }
  }
}
</script>
