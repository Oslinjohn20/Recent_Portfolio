<template>
  <v-container grid-list-xl>
    <h2 class="pl-4">
      <span>Web</span>
      <span class="blue--text">Portfolio</span>
    </h2>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-dialog v-model="project.dialog" lazy max-width="1000" v-for="project in projects" :key="project.title">
        <template v-slot:activator="{ on }">
          <v-flex xs12 sm6 md4 lg4 xl4 v-on="on">
            <v-card hover flat color="transparent">
              <v-img :src="project.poster" :alt="project.title" height="230"
                lazy-src="https://cdn.dribbble.com/users/503653/screenshots/3143656/fluid-loader.gif"></v-img>
              <v-card-title primary-title class="justify-center">{{ project.title }}</v-card-title>
            </v-card>
          </v-flex>
        </template>
        <v-card v-if="project.dialog">
          <v-img :src="project.poster"></v-img>
          <v-card-text>
            <h3 class="headline mb-0">
              <span>Technology</span>
            </h3>
            <v-chip color="blue" text-color="white">{{ project.tech.tech1 }}</v-chip>
            <v-chip color="blue" text-color="white">{{ project.tech.tech2 }}</v-chip>
            <v-chip color="blue" text-color="white">{{ project.tech.tech3 }}</v-chip>
            <v-chip color="blue" text-color="white">{{ project.tech.tech4 }}</v-chip>
          </v-card-text>
          <v-card-actions>
            <v-btn flat large dark color="blue" :href="project.git" target="_blank">
              <v-icon left>fab fa-github</v-icon>GitHub
            </v-btn>
            <v-btn large flat dark color="blue" :href="project.demo" target="_blank">
              <v-icon left>fas fa-desktop</v-icon>Demo
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-dialog>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  metaInfo: {
    title: 'Web Portfolio',
    titleTemplate: "%s ← Oslin's Portfolio",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      { name: 'description', content: "Oslin Johnson's Portfolio" },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Oslin' " },
      { property: 'og:site_name', content: "Oslin'" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://oslinj-dark.netlify.app/' },
      {
        property: 'og:image',
        content: 'https://i.postimg.cc/NFfwBrrk/Untitled-design.jpg'
      },
      { property: 'og:description', content: "Oslin Johnson's Portfolio" }
    ]
  },
  data() {
    return {
      dialog: false,
      projects: [
        {
          dialog: false,
          title: 'Logan Kitchen',
          git: 'https://github.com/Oslinjohn20/Logan-s_kitchen',
          demo: 'https://loganskitchen.netlify.app/',
          tech: {
            tech1: 'HTML',
            tech2: 'JavaScript',
            tech3: 'CSS'

          },
          poster: 'https://i.postimg.cc/XYv7BxGt/image.png'
        },
        {
          dialog: false,
          title: 'Dark Portfolio',
          git: 'https://github.com/Oslinjohn20/darkPortfolio',
          demo: 'https://oslinj-dark.netlify.app/',
          tech: {
            tech1: 'HTML',
            tech2: 'CSS',
            tech4: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/Jz9V7QbN/image.png'
        },
        {
          dialog: false,
          title: 'Admin Dashboard',
          git: 'n/a',
          demo: 'https://dreamy-johnson-84d509.netlify.app/',
          tech: {
            tech1: 'VUE',
            tech2: 'Node Js',
            tech3: 'HTML',
            tech4: 'JavaScript',
            tech5: 'PostgrSQL'
          },
          poster: 'https://i.postimg.cc/25VQG4JK/image.png'
        },
        {
          dialog: false,
          title: 'Hulu Clone ',
          git: 'https://github.com/Oslinjohn20/Hulu-landing',
          demo: 'https://fascinating-frangollo-122b0c.netlify.app/',
          tech: {
            tech1: 'HTML',
            tech2: 'CSS',
            tech3: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/0yLYt6s5/image.png'
        },
        {
          dialog: false,
          title: 'Starbucks Clone Challenge',
          git: 'https://github.com/Oslinjohn20/starbucks-landing',
          demo: 'https://snowball-test.netlify.com/',
          tech: {
            tech1: 'HTML',
            tech2: 'CSS',
            tech3: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/BbrZWGQF/image.png'
        },
        {
          dialog: false,
          title: 'NetFlix Clone Challenge',
          git: 'https://github.com/Oslinjohn20/NextClone',
          demo: 'https://soft-dango-d8e27e.netlify.app/',
          tech: {
            tech1: 'HTML',
            tech2: 'CSS',
            tech3: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/436WVv9R/image.png'
        },
        {
          dialog: false,
          title: 'Calendar ',
          git: 'https://github.com/Oslinjohn20/Vuetify-calendar-firestore',
          demo: 'https://capable-rolypoly-2ba279.netlify.app/',
          tech: {
            tech1: 'VUE',
            tech2: 'Vuex',
            tech3: 'Firebase',
            tech4: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/x8MyHM8b/image.png'
        },
        {
          dialog: false,
          title: 'Quiz Time ',
          git: 'https://github.com/Oslinjohn20/QuizTime',
          demo: 'https://unrivaled-empanada-06769d.netlify.app/',
          tech: {
            tech1: 'HTML',
            tech2: 'CSS',
            tech3: 'JavaScript'
          },
          poster: 'https://i.postimg.cc/DzHz8qWG/image.png'
        }

      ]
    }
  }
}
</script>

<style  scoped></style>
