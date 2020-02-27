<template>
  <div>
    <v-app-bar class="h-appbar" elevation="0" dense>
      <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
      <v-spacer></v-spacer>
      <!-- <h2>{{title}}</h2>
      <v-spacer></v-spacer>-->
      <v-btn
        outlined
        href="https://drive.google.com/file/d/1-C5ze3CY6OJnve9Y6EXXaZqMV1vxqWJv/view"
        target="_blank"
      >
        <v-icon>mdi-paperclip</v-icon>
        <span>Resume</span>
      </v-btn>
    </v-app-bar>
    <div
      v-bind:class="{'h-toolbar': $vuetify.breakpoint.mdAndUp, 'h-disable' :$vuetify.breakpoint.smAndDown}"
    >
      <v-btn
        text
        class="mt-1"
        v-for="(item, i) in items"
        :key="i"
        @click="onClickMenu(item.link)"
      >{{item.title}}</v-btn>
    </div>

    <Navigation v-model="drawer" @onClickMenu="onClickMenu"></Navigation>
  </div>
</template>

<style scoped>
.h-appbar {
  background-color: transparent !important;
  position: fixed !important;
  z-index: 3;
}
.h-toolbar {
  margin-left: 55px;
  width: 35%;
  height: 63px;
  position: absolute;
  z-index: 4;
}
.h-disable {
  display: none;
}
</style>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Prop } from "vue-property-decorator";
import Navigation from "@/components/Navigation.vue";

@Component({
  components: {
    Navigation
  }
})
export default class AppBar extends Vue {
  @Prop()
  title!: string;

  value2 = "masih sama";

  drawer = false;
  items = [
    { title: "About", link: "about" },
    { title: "Project", link: "project" },
    { title: "Contact", link: "contact" }
  ];

  onClickMenu(link: String) {
    this.$emit("onMenu", link);
  }
  getvalue(links: string) {
    this.value2 = links;
  }
  changeValue(link: string) {
    this.value2 = link;
  }
}
</script>