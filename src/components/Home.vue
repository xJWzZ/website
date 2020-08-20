<template>
<v-app>
  <v-parallax :src="background.src" height="1000" dark fluid>
  <v-container>
    <v-layout row wrap justify-space-between>
      <v-flex xs12 md6 class="ma-10">
        <h1 class='display-4'>Professional Summary</h1>
      </v-flex>
      <v-flex xs12 md4 class="ma-10">
        <p class="body-1" >
          Highly ambitious Software Engineer Graduate with a background in Java, Python and Javascript.
        </p>
        <p>
          Experience in Javascript frameworks such as Vue and React. Experience in Python frameworks such as Flask.
        </p>
        <p>
          Deadline-driven Engineer able to
          work under tight schedules and limited budgets to achieve innovative designs that meet and exceed objectives. Familiar
          with Agile Development.
        </p>
      </v-flex>
    </v-layout>
  </v-container>
  <!-- <v-container class="ma-10">

  </v-container>
  <v-container  class="mt-10" fluid>
  <v-carousel height="600">
    <v-carousel-item
    v-for="(image, i) in photos"
    :key="i"
    :src="image.src"
    reverse-transition="fade-transition"
    transition="fade-transition"
    >
    </v-carousel-item>
  </v-carousel>
</v-container> -->
</v-parallax>
</v-app>
</template>

<script>
export default {
  name: 'Home',

  data: () => ({
    drawer: false,
    drawerRight: null,
    right: false,
    left: false,
    background: {
      src: require('@/assets/website_backgroung_test.jpg_1.jpg')
    },
    photos: [
      {
        src: require('@/assets/carousel_photos/1.jpg')
      },
      {
        src: require('@/assets/carousel_photos/2.jpg')
      },
      {
        src: require('@/assets/carousel_photos/3.jpg')
      },
      {
        src: require('@/assets/carousel_photos/4.jpg')
      },
      {
        src: require('@/assets/carousel_photos/5.jpg')
      },
      {
        src: require('@/assets/carousel_photos/8.jpg')
      },
      {
        src: require('@/assets/carousel_photos/9.jpg')
      }
    ]
  })
}
</script>

<style scoped>
  /* p { */
    /* color: #303030 */
  /* } */
</style>
