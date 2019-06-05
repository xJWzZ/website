<template>
  <v-app id="inspire" dark>
    <v-navigation-drawer
      v-model="drawer"
      clipped
      fixed
      app
    >
      <v-list dense>
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>dashboard</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Dashboard</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
        <v-list-tile @click="">
          <v-list-tile-action>
            <v-icon>settings</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title>Settings</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left>
      <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
      <v-toolbar-title>Jack Wall</v-toolbar-title>
    </v-toolbar>
    <v-content>

      <v-container fluid fill-height>
          <!-- <v-parallax src="/astronomy-1867616_1920.jpg"> -->

            <v-layout justify-center align-center>
                <!-- <v-card color="cyan darken-2" class="white--text"> -->
              <v-flex shrink>

                <blockquote class="blockquote">
                    Welcome to my website. Lets take a look at it lads
                </blockquote>

                <div>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                        Harum maiores modi quidem veniam, expedita quis laboriosam,
                        ullam facere adipisci, iusto, voluptate sapiente corrupti asperiores
                        rem nemo numquam fuga ab at.
                    </p>
                    <p>
                        Lorem ipsum dolor sit amet, consectetur adipisicing elit. Harum maiores
                        modi quidem veniam, expedita quis laboriosam, ullam facere adipisci,
                        iusto, voluptate sapiente corrupti asperiores rem nemo numquam fuga ab at.
                    </p>
                </div>

              </v-flex>
              <!-- </v-card> -->
            </v-layout>
        <!-- </v-parallax> -->
      </v-container>
    </v-content>
    <v-footer app fixed>
      <span>Jack Wall, UCC Computer Science Student</span>
    </v-footer>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: false
    }),
    props: {
      source: String
    }
  }
</script>
