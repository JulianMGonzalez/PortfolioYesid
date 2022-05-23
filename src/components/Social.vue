<template>
  <ul class="social">
    <li v-for="(social, i) in socialList" :key="i">
      <a :href="social.link" target="_blank" rel="noreferrer"
        ><img class="svg" :src="social.src" alt="social"
      /></a>
    </li>
  </ul>
  <!-- End. social -->
</template>

<script>
export default {
  data() {
    return {
      socialList: [
        {
          link: "https://www.facebook.com/Yesid.Valenzuela",
          src: require("../assets/img/svg/social/facebook.svg"),
        },
        {
          link: "https://twitter.com/yesidvh",
          src: require("../assets/img/svg/social/twitter.svg"),
        },
        {
          link: "https://www.instagram.com/yesidvh",
          src: require("../assets/img/svg/social/instagram.svg"),
        },
        {
          src: require("../assets/img/svg/social/youtube.svg"),
          link: "youtube.com/channel/UC8ipUz9xUTQg4ApmY-yRqJQ/featured",
        },
        {
          src: require("../assets/img/svg/social/tik-tok.svg"),
          link: "https://www.tiktok.com/@viviendoes",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
