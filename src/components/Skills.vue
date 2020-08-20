<template>
<v-app>
  <v-parallax :src="background.src" height="800" dark fluid>
  <v-container>
    <v-layout row wrap justify-space-between>
      <v-flex xs12 md6 class="ma-8">
        <h1 class='display-2'>Mapbox Development</h1>
      </v-flex>
      <v-flex>
        <mapbox
          :access-token="access_token"
          :map-options="map_options"
          @map-load="loaded"
          @map-zoomend="zoomend"
          @map-click:points="clicked"
        />
      </v-flex>

    </v-layout>
  </v-container>
</v-parallax>
</v-app>
</template>

<script>
import Mapbox from 'mapbox-gl-vue'

export default {
  name: 'Skills',

  components: { Mapbox },

  data: () => ({
    map_options: {
      style: 'mapbox://styles/mapbox/dark-v10',
      center: [-65.54764911708693, 40.436532223282285],
      zoom: 2,
      dragRotate: false
    },
    access_token: 'pk.eyJ1IjoiamFja3cxOTk3IiwiYSI6ImNqdHNxeHNvOTB5cTg0ZG83bnpnZzRjazEifQ.UC6s7pbeVV1LvWhniKdYDg',
    background: {
      src: require('@/assets/website_backgroung_test.jpg_1.jpg')
    }

  }),

  methods: {
    loaded (map) {
      map.addLayer({
        id: 'points',
        type: 'symbol',
        source: {
          type: 'geojson',
          data: {
            type: 'FeatureCollection',
            features: [
              {
                type: 'Feature',
                geometry: {
                  type: 'Point',
                  coordinates: [-9.504678758655274, 52.44537982898913]
                },
                properties: {
                  title: 'Home',
                  icon: 'suitcase'
                }
              },
              {
                type: 'Feature',
                geometry: {
                  type: 'Point',
                  coordinates: [-122.414, 37.776]
                },
                properties: {
                  title: 'J1 Summer 2018',
                  icon: 'airport'
                }
              }
            ]
          }
        },
        layout: {
          'icon-image': '{icon}-15',
          'text-field': '{title}',
          'text-font': ['Open Sans Semibold', 'Arial Unicode MS Bold'],
          'text-offset': [0, 0.6],
          'text-anchor': 'top'
        },
        paint: {
          'text-color': '#ffffff'
          // 'icon-size': 15
        }
      })
    },
    zoomend (map, e) {
      console.log('Map zoomed')
    },
    clicked (map, click) {
      // const title = click.features[0].properties.title
      // console.log(click.lngLat)
      map.flyTo({
        center: click.features[0].geometry.coordinates,
        speed: 0.4,
        zoom: 9
      })
    }
  }

}
</script>

<style>
#map {
  width: 100%;
  height: 500px;
}
</style>
