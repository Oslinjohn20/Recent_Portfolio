<template>
  <v-layout row justify-center align-center wrap class="mt-4 pt-2">
    <v-flex xs12 sm12 md5 lg6 xl6 class="mt-4 pt-4">
      <h2 class="mb-4 pl-4 pt-2">Education</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">MARCH 2020 -</div>
                <div class="caption font-weight-bold green--text">AUG 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Full Stack Web Development Course</strong>
                <div class="caption mb-2">Life Choices Coding Academy</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">MAY 2012 -</div>
                <div class="caption font-weight-bold green--text">APRIL 2013</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Motor Mechanics (Petrol)</strong>
                <div class="caption mb-2">North Link College</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">MAY 2013 -</div>
                <div class="caption font-weight-bold green--text">APRIL 2017</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Motor Mechanic</strong>
                <div class="caption mb-2">Imperial Technical Training Academy</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-flex xs12 sm12 md4 lg6 xl6 class="mt-4 pt-2">
      <h2 class="mb-4 pl-4">Experience</h2>
      <v-card-text class="py-0">
        <v-timeline align-top dense>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">JULY 2021 -</div>
                <div class="caption font-weight-bold green--text">PRESENT</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Junior Lecturer</strong>
                <div class="caption mb-2">Life Choice Coding Academy</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">AUG 2020 -</div>
                <div class="caption font-weight-bold green--text">SEPT 2021</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Web developer Intern</strong>
                <div class="caption mb-2">Life Choices Studio</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>

          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">AUG 2017 -</div>
                <div class="caption font-weight-bold green--text">JAN 2020</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>General Worker</strong>
                <div class="caption mb-2">Lourens ROadmarking</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">SEPT 2013 -</div>
                <div class="caption font-weight-bold green--text">JUN 2015</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Motor Mechanic Apprentice</strong>
                <div class="caption mb-2">Engine & Gearbox Exchange</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
          <v-timeline-item color="green" small>
            <v-layout pt-3>
              <v-flex xs4>
                <div class="caption font-weight-bold green--text">FEB 2013-</div>
                <div class="caption font-weight-bold green--text">AUG 2013</div>
              </v-flex>
              <v-flex class="pl-2">
                <strong>Motor Mechanic Apprentice</strong>
                <div class="caption mb-2">Hyundai Paardien Eiland</div>
              </v-flex>
            </v-layout>
          </v-timeline-item>
        </v-timeline>
      </v-card-text>
    </v-flex>
    <v-layout row justify-center align-center wrap class="mt-4 pt-2">
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Design</span>

          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>Figma</strong>
        <v-progress-linear v-model="buffer1" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>

      </v-flex>
      <v-flex xs12 sm12 md4 lg5 xl5 class="mx-2 pt-4">
        <h2>
          <span>Coding</span>
          <span class="green--text">Skills</span>
        </h2>
        <br>
        <strong>VUE</strong>
        <v-progress-linear v-model="buffer4" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>HTML/CSS</strong>
        <v-progress-linear v-model="buffer5" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
        <strong>JavaScript</strong>
        <v-progress-linear v-model="buffer6" :buffer-value="bufferValue" color="green" height="16"></v-progress-linear>
      </v-flex>
      <div class="mt-4 pt-2">
        <v-btn
          href="https://docs.google.com/document/d/1wRjN4D_hV8OqbZZ4Ef0RczueOl0EHhxuCM9dz3FMhDA/edit?usp=sharing"
          target="_blank"
          color="green"
          dark
          large
        >
          Download Resume
          <v-icon right dark>fas fa-file-download</v-icon>
        </v-btn>
      </div>
    </v-layout>
  </v-layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Resume',
    titleTemplate: "%s ← Oslin's Room",
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
        name: 'description',
        content:
          'Vue  HTML CSS JavaScript Design Figma Coding Skills Resume Work Web Developer Front-End'
      },
      { charset: 'utf-8' },
      { property: 'og:title', content: "Oslin's Room" },
      { property: 'og:site_name', content: "Oslin's Room" },
      { property: 'og:type', content: 'website' },
      { property: 'og:url', content: 'https://oslinj-dark.netlify.app/' },
      {
        property: 'og:image',
        content: 'https://i.postimg.cc/NFfwBrrk/Untitled-design.jpg'
      },
      {
        property: 'og:description',
        content:
          'Vue HTML CSS JavaScript Design Figma Coding Skills Resume Work Web Developer Front-End'
      }
    ]
  },
  data () {
    return {
      value: 0,
      buffer1: 0,
      buffer2: 0,
      buffer3: 0,
      buffer4: 0,
      buffer5: 0,
      buffer6: 0,
      bufferValue: 100,
      interval: 0
    }
  },
  mounted () {
    this.startBuffer()
  },

  beforeDestroy () {
    clearInterval(this.interval)
  },

  methods: {
    startBuffer () {
      this.interval = setInterval(() => {
        this.buffer1 = 90
        this.buffer2 = 85
        this.buffer3 = 80
        this.buffer4 = 80
        this.buffer5 = 90
        this.buffer6 = 70
      }, 800)
    }
  }
}
</script>
<style >
</style>
