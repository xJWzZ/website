<template>
  <div class="skills">
    <v-card>
      <v-parallax :src="background.src" height="1000">
        <v-container>
          <v-layout row wrap justify-space-between>
            <v-flex xs12 md12>
              <h1 class='display-4 mb-5'>Skills & Projects</h1>
            </v-flex>
            <v-flex xs12 md6>
              <h2>Hard Skills</h2>
              <ul>
                <li>
                  Proficiency in the following programming languages:
                  <ul>
                    <li v-for='hard_skill in hard_skills' :key='hard_skill.heading'>
                      <h4>{{hard_skill.heading}}</h4>
                      <p>
                        {{hard_skill.description}}
                      </p>
                    </li>
                  </ul>
                </li>
              </ul>
            </v-flex>
            <v-flex xs12 md6>
              <h2>Soft Skills</h2>
              <ul>
                <li>
                  <h4>Independent and mobile worker</h4>
                  <p>
                    Worked in San Francisco on Pier 39 as part
                    of the J1 visa program.
                  </p>
                </li>
                <li>
                  <h4>Leadership skills</h4>
                  <p>
                    Elected Men's Captain of UCC Ultimate Frisbee team. Role
                    involves picking teams, leading by example, helping teammates, and attending
                    over 95% of trainings.
                  </p>
                  <p>
                    See <a href="https://www.youtube.com/watch?v=WBNldW9QVSU&app=desktop">here</a> me captaining UCC at the indoor semi finals on February 16th 2020 in which we lost to DCU
                  </p>
                </li>
              </ul>
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
    hard_skills: [
      { heading: 'Javascript', description: 'Spent 3 months on work placement learning VueJS framework with concentrated emphasis on functional programming practices.' },
      { heading: 'Python', description: '4 years of college programming experience, covering areas such as artificial intellegence, network and data communications, and database management.' },
      { heading: 'Haskell', description: '1 year of college programming experience learning about functional programming practices and techniques.' },
      { heading: 'C++', description: '1 year of college programming experience using micro-controllers to recreate traffic lights, LED signs, and kids games. Components used were LED monitors, buzzers, a bread board and many, many pins and wires!' },
      { heading: 'HTML, CSS, PHP, GoLang', description: 'Experience from various Computer Science modules across the 4 years, as well as personal projects and exploration.' }
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
