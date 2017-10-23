<template>
  <div class="center" style="width:720px">
    <v-container>
      <v-layout row wrap>
      <v-flex xs12 sm6 class="text-xs-center text-sm-right">
        <v-btn large router to="/meetups" class="info">Explore Meetups</v-btn>
      </v-flex>
        <v-flex xs12 sm6 class="text-xs-center text-sm-left">
        <v-btn large router to="/meetup/new" class="info">Organize Meetup</v-btn>
      </v-flex>
      </v-layout>
      <v-layout row wrap style="height:50vh">
        <v-flex xs12>
      <v-carousel hide-controls style="height:75%">
        <v-carousel-item
         v-for="(item,i) in items"
         v-bind:src="item.src"
         :key="i"></v-carousel-item>
      </v-carousel>
    </v-flex>
  </v-layout>
    </v-container>
  </div>
</template>
<script>
  export default {
    data () {
      return {
        items: [
          {
            src: '/static/doc-images/carousel/squirrel.jpg'
          },
          {
            src: '/static/doc-images/carousel/sky.jpg'
          },
          {
            src: '/static/doc-images/carousel/bird.jpg'
          },
          {
            src: '/static/doc-images/carousel/planet.jpg'
          }
        ]
      }
    }
  }
</script>
