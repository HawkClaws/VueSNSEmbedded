<template>
  <div>
    <div class="youtube">
      <iframe
        width="100%"
        height="100%"
        :src="'https://www.youtube.com/embed/' + youtubeId"
        title="YouTube video player"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>

<style scoped>
.youtube {
  position: relative;
  width: 100%;
  padding-top: 56.25%;
}
.youtube iframe {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
}
</style>

<script lang="ts">
import { ref, defineComponent } from "vue";
export default defineComponent({
  name: "Youtube",
  props: {
    youtubeId: {
      type: String,
      required: true
    }
  },
  mounted() {},
  methods: {}
});
</script>

