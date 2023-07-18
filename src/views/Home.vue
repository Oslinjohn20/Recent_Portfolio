<template>
  <v-layout column justify-center align-center class="mt-2 pt-1">
    <VueCompareImage class="hidden-md-and-down" hover :style="{ minWidth: '800px' , maxHeight: '500px'}" :sliderLineWidth="sliderLine"
      :handleSize="hSize" :leftImage="leftImage" :rightImage="rightImage" :sliderPositionPercentage="sliderPosition" />
    <VueCompareImage class="hidden-lg-and-up" hover :style="{ maxWidth: '400px' }" :sliderLineWidth="sliderLine"
      :handleSize="hSize" :leftImage="leftImage2" :rightImage="rightImage2" :sliderPositionPercentage="sliderPosition" />

    <br>

    <vue-typer class="headline" :repeat="0" text="Oslin Johnson"></vue-typer>
    <vue-typer :text="text1" :repeat="Infinity" :shuffle="false" initial-action="erasing" :pre-type-delay="70"
      :type-delay="70" :pre-erase-delay="1980" :erase-delay="150" erase-style="select-back" :erase-on-complete="false"
      caret-animation="smooth"></vue-typer>
    <br>
    <v-flex xs12 sm6 md4 lg4 xl4>
      <v-card flat color="transparent" max-width="500">
        <v-card-title primary-title>
          <div>
            <h3 class="headline mb-0">
              <span>About</span>
              <span class="blue--text">Me</span>
            </h3>
            <div>
              <p>
                Hello! I’m Oslin Johnson. I'm a front-end developer who
                is passionate about
                <span class="blue--text font-weight-bold">VUE</span>, building user experiences,
                fighting for simplicity over complexity and constantly learning.
                When I'm not coding I am teaching coding to youth from the Cape Flats area to ensure they are able to
                succeed dispite their conditions.
              </p>
            </div>
          </div>
        </v-card-title>

        <v-card-actions class="hidden-sm-and-down">
          <v-btn v-for="icon in icons" :key="icon.icon" fab dark outline color="blue" :href="icon.href" target="_blank">
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>

        <v-card-actions class="hidden-md-and-up justify-center">
          <v-btn v-for="icon in icons" :key="icon.icon" small fab dark outline color="blue" :href="icon.href"
            target="_blank">
            <v-icon dark>{{ icon.icon }}</v-icon>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import { VueTyper } from 'vue-typer'
import VueCompareImage from 'vue-compare-image'

export default {
  metaInfo: {
    title: 'Home',
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
  components: {
    'vue-typer': VueTyper,
    VueCompareImage
  },
  data () {
    return {
      icons: [
        { href: 'https://github.com/Oslinjohn20', icon: 'fab fa-github' },

        { href: 'https://twitter.com/Ossiekc26', icon: 'fab fa-twitter' },
        {
          href: 'https://www.linkedin.com/in/oslin-johnson-9400691ab',
          icon: 'fab fa-linkedin-in'
        }
      ],
      text1: ['Front-End Developer', 'Web Developer', 'Lecturer'],
      leftImage: 'https://i.postimg.cc/NFfwBrrk/Untitled-design.jpg',
      rightImage: 'https://i.postimg.cc/qBy8qMNd/Full-HD.jpg',
      leftImage2: 'https://i.postimg.cc/P5zh7b9F/Untitled-design-1-1.jpg',
      rightImage2: 'https://i.postimg.cc/KcP2jDvc/Full-HD-1.jpg',
      sliderLine: 0,
      hSize: 0,
      sliderPosition: 0.5
    }
  }
}
</script>
<style>
@keyframes rocking {

  0%,
  100% {
    transform: rotateZ(-10deg);
  }

  50% {
    transform: rotateZ(10deg);
  }
}

.vue-typer {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
  font-size: 20px;
  font-weight: 700;
}

.vue-typer .custom.char.typed {
  color: rgb(0, 117, 128);
}

.vue-typer .custom.char.selected {
  color: #e91e63;
}

.vue-typer .custom.caret {
  animation: rocking 1s ease-in-out 0s infinite;
}

.vue-typer .custom.caret.typing {
  background-color: rgb(0, 117, 128);
}

.vue-typer .custom.caret.selecting {
  display: inline-block;
  background-color: #e91e63;
}
</style>
