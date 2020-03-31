<template>
  <div class="education">
    <v-card>
      <v-parallax :src="background.src" height="1200">
        <v-container>
          <v-layout row wrap justify-space-between>
            <v-flex xs12 md12>
              <h1 class='display-4 mb-5'>Education</h1>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-2 mt-4">3rd Year Exam Results</h2>
              <h3 class="title">First Class Honours (>70%)</h3>
              <p>Best Module Results:</p>
              <v-list-item v-for="grade in third_year_grades" :key="grade.module">
                <v-list-item-content>
                <v-list-item-title>{{grade.module}} - {{grade.result}}%</v-list-item-title>
              </v-list-item-content>
              </v-list-item>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-2 mt-4">2nd Year Exam Results</h2>
              <h3 class='title'>Second Class Honours (>60%)</h3>
              <p>Best Module Results:</p>
              <v-list-item v-for="grade in second_year_grades" :key="grade.module">
                <v-list-item-content>
                  <v-list-item-title>{{grade.module}} - {{grade.result}}%</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
            </v-flex>
            <v-flex xs12 md6>
              <h2 class="display-2 mt-4">Leaving Certificate</h2>
              <h3 class='title'>530/625 points</h3>
              <v-list-item v-for="grade in leaving_cert" :key="grade.module">
                <v-list-item-content>
                  <v-list-item-title>{{grade.module}} - {{grade.result}}</v-list-item-title>
                </v-list-item-content>
              </v-list-item>
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
      { module: 'Maths', result: 'A1 (90%+)' },
      { module: 'Physics', result: 'A2 (85%+)' },
      { module: 'Music', result: 'B1 (80%+)' },
      { module: 'Chemistry', result: 'B3 (70%+)' },
      { module: 'English', result: 'B3 (70%+)' },
      { module: 'French', result: 'C1 (65%+)' }
    ]
  })
}
</script>
