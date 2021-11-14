<template>
  <div class="instagram-media-center">
    <blockquote class="instagram-media">
      <a :href="'https://www.instagram.com/p/'+instagramId"></a>
    </blockquote>
  </div>
</template>
<style scoped>
  .instagram-media-center {
    width: 324px !important;
    margin-left: auto;
    margin-right: auto;
  }
</style>
<script lang="ts">
import { ref, defineComponent } from "vue";
export default defineComponent({
  name: "Instagram",
  props: {
    instagramId: {
      type: String,
      required: true
    }
  },
  mounted() {
    setTimeout(() => {
      let instagramScript = document.createElement("script");
      instagramScript.setAttribute("src", "https://www.instagram.com/embed.js");
      instagramScript.setAttribute("async", "true");
      document.head.appendChild(instagramScript);
    }, 100);
  },
  methods: {}
});
</script>
