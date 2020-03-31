<template>
  <div class="awards">
    <v-card>
      <v-parallax :src="background.src" height="1000">
        <v-container>
          <v-layout row wrap justify-space-between>
            <v-flex xs12 md12>
              <h1 class='display-4 mb-5'>Awards & Achievements</h1>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-1 mt-4"><a href="http://kerryseyephotosales.photoshelter.com/image/I0000Bc5O8.Vijk8">Scifest Maths in Science Award 2014</a></h2>
              <p class="title font-weight-light">
                Project on predicting the specs and release date of the next generation of playstation console using statistics.
              </p>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-1 mt-4">Team Math Regional Round Winner 2016</h2>
              <p class="title font-weight-light">
                Captain of the Secondary School Math team to win the Regional Competition.
              </p>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-1 mt-4">St. Michael’s Math and Science Award</h2>
              <p class="title font-weight-light">
                Awarded greatest math and science performance in the class for years 2014, 2015, 2016
              </p>
            </v-flex>
          </v-layout>
        </v-container>
      </v-parallax>
  </v-card>
  </div>
</template>

<script>
export default {
  data: () => ({
    background: {
      src: require('@/assets/website_backgroung_test.jpg_1.jpg')
    },
    third_year_grades: [
      { module: 'Software Engineering', result: 74, description: 'The benefits and history of Software development techniques.' },
      { module: 'Middleware', result: 70, description: 'Learned of features and performance benefits within the use of Middleware.' },
      { module: 'Workplace Technology and Skills', result: 89, description: 'Learned about the workplace, picking up a brand new language, and being able to present to a group of your peers.' },
      { module: 'Team Software Project', result: 70, description: 'Work on a team of 7-8 people to develop a product using Software development techniques.' }
    ],
    second_year_grades: [
      { module: 'Algorithms and Data Structures 1', result: 75 },
      { module: 'Algorithms and Data Structures 2', result: 80 },
      { module: 'Intermediate Programming', result: 84 },
      { module: 'Computer Architecture', result: 75 }
    ],
    leaving_cert: [
      { module: 'Maths', result: 'A1' },
      { module: 'Physics', result: 'A2' },
      { module: 'Music', result: 'B1' },
      { module: 'Chemistry', result: 'B3' },
      { module: 'English', result: 'B3' },
      { module: 'French', result: 'C1' }
    ]
  })
}
</script>
