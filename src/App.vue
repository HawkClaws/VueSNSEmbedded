<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup
import Instagram from "./components/embedded/Instagram.vue";
import Twitter from "./components/embedded/Twitter.vue";
import Youtube from "./components/embedded/Youtube.vue";
</script>

<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <div style="display:flex;">
    <Instagram style="width:300px; margin:0 50px" instagramId="BsOGulcndj-" />
    <Twitter style="width:300px; margin:0 50px" twitterId="896523232098078720" />
    <Youtube style="width:450px; margin:0 50px" youtubeId="XqZsoesa55w" />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
