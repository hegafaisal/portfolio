<template>
  <v-navigation-drawer class="h-nav" v-model="drawer" fixed>
    <v-icon class="ml-4 mt-4" color="white" @click="drawer = !drawer">mdi-window-close</v-icon>
    <v-row>
      <v-col>
        <h1
          v-for="(item, x) in items"
          :key="x"
          @click="onClickmenu(item.link); drawer = !drawer"
          class="my-12 ml-12 pl-12 title-pointer"
        >{{item.title}}</h1>
      </v-col>
    </v-row>
  </v-navigation-drawer>
</template>

<style scoped>
.h-nav {
  width: 100% !important;
  background-color: #333333 !important;
}
.h-nav h1 {
  color: white;
}
.title-pointer {
  cursor: pointer;
}
</style>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";
import { Prop } from "vue-property-decorator";

@Component
export default class Navigation extends Vue {
  @Prop()
  value!: any;
  about = "about";
  get drawer() {
    return this.value;
  }
  set drawer(val: any) {
    this.$emit("input", val);
  }
  onClickmenu(link: string) {
    this.$emit("onClickMenu", link);
  }
  items = [
    { title: "About", link: "about" },
    { title: "Project", link: "project" },
    { title: "Contact", link: "contact" }
  ];
}
</script>
