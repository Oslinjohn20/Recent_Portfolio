<template>
  <v-app :dark="goDark">
    <v-content>
      <v-container align-center>
        <TheHeader :goDark="goDark" @changeTheme="updateTheme($event)" />

        <transition name="router-animation" mode="out-in" enter-active-class="animated fadeIn fast"
          leave-active-class="animated fadeOut faster">
          <router-view></router-view>
        </transition>
      </v-container>
    </v-content>
    <TheFooter />
  </v-app>
</template>

<script>
import TheHeader from './components/TheHeader'
import TheFooter from './components/TheFooter'

export default {
  name: 'App',
  metaInfo: {
    title: 'Home',
    titleTemplate: "%s ← Oslin's Room",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'description', content: "Oslin Johnson's Portfolio" },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Oslin' Room" },
      { property: 'og:site_name', content: "Oslin' Room" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'ttps://oslinj-dark.netlify.app' },
      {
        property: 'og:image',
        content: '../public/resized-removebg-preview (1).png'
      },
      { property: 'og:description', content: "Oslin Johnson's Portfolio" }
    ]
  },
  components: {
    TheHeader,
    TheFooter
  },
  data () {
    return { goDark: false }
  },
  methods: {
    updateTheme (updatedTheme) {
      this.goDark = !updatedTheme
    }
  }
}
</script>
<style>
@import "https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.7.0/animate.min.css";
::-webkit-scrollbar{
  display: none;
}
</style>
