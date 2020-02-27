<template>
  <v-app class="scroll">
    <router-view></router-view>
  </v-app>
</template>

<style scoped>
.scroll {
}
</style>

<script lang="ts">
import Vue from "vue";
import Component from "vue-class-component";

@Component
export default class App extends Vue {}
</script>
