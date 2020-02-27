<template>
  <div>
    <!-- AppBar -->
    <Appbar @onMenu="onMenu" title="My Protofolio"></Appbar>

    <div class="h-content">
      <div
        class="h-content-about about"
        v-bind:style="[
          $vuetify.breakpoint.smAndDown
            ? { height: auto }
            : { height: windowHeight + 'px' },
          { backgroundImage: 'url(' + images.background2 + ')' }
        ]"
      >
        <!-- for content about -->
        <div class="content_center">
          <div class="content_center--inner">
            <h1>
              Hi, I'm Hega Faisal Agustian. An aspiring mobile developer who is
              interested in Flutter and designing a UX for mobile development.
            </h1>
          </div>
        </div>
      </div>
      <div class="freespace" :style="{ backgroundImage: 'url(' + images.background1 + ')' }"></div>
      <div
        class="h-content-project project"
        v-bind:style="[
          $vuetify.breakpoint.smAndDown
            ? { height: auto }
            : { height: windowHeight + 'px' },
          { backgroundImage: 'url(' + images.background2 + ')' }
        ]"
      >
        <!-- for content project -->

        <h3 class="h-2 ml-12 pt-12">Project For Preview</h3>
        <v-container class="my-5">
          <v-layout row wrap>
            <v-flex sm6 md6 lg6 xs12 class="px-6 py-3">
              <v-img src="@/assets/app1.png" height="350px" contain />
            </v-flex>
            <v-flex sm6 md6 lg6 xs12 class="px-6 py-3">
              <h3>Sewain</h3>
              <p>
                "sewain" is an application created to complete a thesis project.
                The application is built using the Flutter SDK and Firebase
                database.
              </p>

              <h4>Source For Preview:</h4>
              <v-icon size="50">mdi-git</v-icon>
            </v-flex>
          </v-layout>
        </v-container>
      </div>

      <div class="freespace" :style="{ backgroundImage: 'url(' + images.background3 + ')' }"></div>
      <div
        class="h-content-contact contact"
        v-bind:style="[
          $vuetify.breakpoint.smAndDown
            ? { height: auto }
            : { height: windowHeight + 'px' },
          { backgroundImage: 'url(' + images.background2 + ')' }
        ]"
      >
        <h3 class="h-2 ml-12 pt-12">Contact</h3>
        <v-container class="my-5">
          <v-layout row wrap class="pt-md-12 mt-md-12 pt-lg-12 mt-lg-12">
            <v-flex sm12 md3 lg3 xs12 class="mt-6 mt-sm-0 mt-md-0 mt-lg-0">
              <v-layout column align-center>
                <v-btn
                  icon
                  href="https://www.instagram.com/hegafaisal/"
                  target="_blank"
                  height="100"
                  width="100"
                >
                  <v-icon size="100">mdi-instagram</v-icon>
                </v-btn>
                <span>@hega_faisal</span>
              </v-layout>
            </v-flex>
            <v-flex sm12 md3 lg3 xs12 class="mt-6 mt-sm-0 mt-md-0 mt-lg-0">
              <v-layout column align-center>
                <v-btn
                  icon
                  href="https://api.whatsapp.com/send?phone=6281385519324"
                  target="_blank"
                  height="100"
                  width="100"
                >
                  <v-icon size="100">mdi-whatsapp</v-icon>
                </v-btn>
                <span>+62813-8551-9324</span>
              </v-layout>
            </v-flex>
            <v-flex sm12 md3 lg3 xs12 class="mt-6 mt-sm-0 mt-md-0 mt-lg-0">
              <v-layout column align-center>
                <v-btn
                  icon
                  href="mailto:hega.faisalagustian@gmail.com"
                  target="_blank"
                  height="100"
                  width="100"
                >
                  <v-icon size="100">mdi-gmail</v-icon>
                </v-btn>
                <span>hega.faisalagustian@gmail.com</span>
              </v-layout>
            </v-flex>
            <v-flex sm12 md3 lg3 xs12 class="mt-6 mt-sm-0 mt-md-0 mt-lg-0">
              <v-layout column align-center>
                <v-btn
                  icon
                  href="https://www.linkedin.com/in/hegafaisal/"
                  target="_blank"
                  height="100"
                  width="100"
                >
                  <v-icon size="100">mdi-linkedin-box</v-icon>
                </v-btn>
                <span>Hega Faisal Agustian</span>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-container>
      </div>
      <div class="freespace" :style="{ backgroundImage: 'url(' + images.background4 + ')' }"></div>
    </div>
    <v-footer class="blue-grey darken-4">
      <v-col class="text-center grey--text text--lighten-3">
        2020 —
        <strong>@hega</strong>
      </v-col>
    </v-footer>
  </div>
</template>

<style scoped>
.content_center {
  max-width: 60rem;
}

.h-appbar h3 {
  color: #333333;
}
.h-content {
  width: 100%;
  background-color: #e1f4f3;
}
.h-content-about {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  height: auto;
  padding: 3.5rem 2rem;
  background-color: #eee;
  background-attachment: fixed;
  background-repeat: repeat;
}
.h-content-project {
  height: auto;
  background-color: #eee;
  background-attachment: fixed;
  background-repeat: repeat;
}
.h-content-contact {
  height: auto;
  background-color: #eee;
  background-attachment: fixed;
  background-repeat: repeat;
}
.freespace {
  min-height: 25vh;
  background-size: cover;
  background-attachment: fixed;
}
.h-disable {
  display: none;
}

.grid_container {
  max-width: 60rem;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 2.5rem;
}

.grid-title {
  grid-column: 1/-1;
  text-align: center;
  margin-bottom: 1.25rem;
}

.grid-card {
  position: relative;
  overflow: hidden;
  -webkit-border-radius: 10px;
  -moz-border-radius: 10px;
  border-radius: 10px;
  box-shadow: 4px 8px 10px rgba(0, 0, 0, 0.06);
}

.grid-card img {
  max-width: 100%;
  display: block;
}

.grid-card:first-of-type {
  background-color: #e0719e;
  color: #fff;
}

.grid-card:last-of-type {
  background-color: #7fd6c2;
  color: #fff;
}

.body_text {
  padding: 2.5rem 2.8rem;
}
</style>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import Appbar from "@/components/Appbar.vue";

@Component({
  components: {
    Appbar
  }
})
export default class Home extends Vue {
  windowHeight = window.innerHeight;
  isMobile = false;
  x = 1;

  images = {
    ///img/background1.170ee42f.jpg
    background1: require("@/assets/background1.png"),
    background2: require("@/assets/background2.png"),
    background3: require("@/assets/background3.png"),
    background4: require("@/assets/background4.png"),
    app1: require("@/assets/app1.png")
  };

  onMenu(link: string) {
    const el = this.$el.getElementsByClassName(link)[0];
    if (el) {
      el.scrollIntoView({ behavior: "smooth" });
    }
  }

  mounted() {
    window.onresize = () => {
      this.windowHeight = window.innerHeight;
    };
  }
  onResize() {
    this.isMobile = window.innerWidth < 600;
  }
}
</script>
