<template>
<v-app>
<v-content>
  <v-carousel height="800">
    <v-carousel-item
    v-for="(image, i) in photos"
    :key="i"
    :src="image.src"
    reverse-transition="fade-transition"
    transition="fade-transition"
    >
    </v-carousel-item>
  </v-carousel>
  <v-card class="mx-auto ma-9" max-width="1200" dark hover >
    <v-card-title >
      <h1 class="display-2 font-weight-medium font-italic" >Professional Summary</h1>
    </v-card-title>
    <v-card-text class="body-1">
      Highly ambitious Software Engineer Graduate with a background in Java, Python and Javascript. Experience in Javascript
frameworks such as Vue and React. Experience in Python frameworks such as Flask. Deadline-driven Engineer able to
work under tight schedules and limited budgets to achieve innovative designs that meet and exceed objectives. Familiar
with Agile Development.
</v-card-text>
  </v-card>
</v-content>
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
        src: require('@/assets/carousel_photos/7.jpg')
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
