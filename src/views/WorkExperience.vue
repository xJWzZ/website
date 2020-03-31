<template>
  <div class="work-experience">
    <v-card height="1000">
      <v-parallax :src="background.src" height="1000">
        <v-container>
          <v-layout row wrap justify-space-between>
            <v-flex xs12 md6>
              <h1 class='display-4'>Work Experience</h1>
            </v-flex>
            <v-flex xs12 md5>
              <h2 class="title">Software Engineer Intern at <a href="https://over-c.com/">Over-C</a></h2>
              <h2 class="title">(March 2019 - August 2019)</h2>
              <p>Worked as a software engineer intern in a fast paced, quickly expanding startup company.</p>
              <p class='mt-4'>Developed an Automated Map Converter that increased efficiency by 50%.</p>
              <p>Tasked with prototyping applications using mesh network sensors for indoor location tracking.</p>
              <p>Visualized user location information into a program using Ubers WebGL-powered framework (deck.gl)</p>
              <p>Used VueJS Javascript Framework to develop a server health report website.</p>
            </v-flex>
            <v-flex xs12 md5>
            </v-flex>
            <v-flex xs12 md5 class="mt-5">
              <h2 class="title">Senior Caddy at <a href="https://www.ballybuniongolfclub.com/">Ballybunion Golf Club</a></h2>
              <h2 class="title">(June 2015 - September 2017)</h2>
              <p>Guided golfers around a highly prestigious golf course which is ranked in
the top 20 golf courses in the world. Memorised course layout with
concentrated emphasis on yards from hole, reading putting green slopes,
and course history. Gained networking capabilities by quickly creating
business connections with golfers on a daily basis.</p>
            </v-flex>
            <v-flex xs12 md5>
            </v-flex>
            <v-flex xs12 md5 class="mt-5">
              <h2 class="title">Self Employed Acoustic Musician</h2>
              <h2 class="title">(August 2016 - Present)</h2>
              <p>Playing gigs both solo and in a band for clubs, bars, weddings and family
celebrations both locally and internationally. Using strong presentation
and preparation skills to create an enjoyable atmosphere while playing.
Performed to crowds of up to 200 people</p>
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
    }
  })
}
</script>
