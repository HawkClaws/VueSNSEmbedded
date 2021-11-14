<template>
  <div>
    <blockquote class="twitter-tweet">
      <a :href="'https://twitter.com/xxxxxxxxxx/status/'+twitterId"></a>
    </blockquote>
  </div>
</template>
<style scoped>
.twitter-tweet {
  margin-left: auto;
  margin-right: auto;
}
</style>
<script lang="ts">
import { ref, defineComponent } from "vue";
export default defineComponent({
  name: "Twitter",
  props: {
    twitterId: {
      type: String,
      required: true
    }
  },
  mounted() {
    setTimeout(() => {
      let tweetScript = document.createElement("script");
      tweetScript.setAttribute(
        "src",
        "https://platform.twitter.com/widgets.js"
      );
      tweetScript.setAttribute("async", "true");
      document.head.appendChild(tweetScript);
    }, 100);
  },
  methods: {}
});
</script>
