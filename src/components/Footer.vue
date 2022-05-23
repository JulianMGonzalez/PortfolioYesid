<template>
  <div class="waxon_tm_copyright">
    <div class="container">
      <div class="copyright_inner">
        <ul>
          <li v-scroll-reveal="{ delay: 20, distance: '20px' }">
            <div class="logo">
              <router-link to="/">
                <img src="../assets/img/logo/logo2.png" width="20%" alt="partners brand" />
              </router-link>
            </div>
            <span>Yesid Valenzuela &copy; {{ new Date().getFullYear() }}</span>

          </li>
          <!-- End li -->

          <li v-scroll-reveal="{ delay: 40, distance: '20px' }">
            <span>Neiva, Huila</span>
            <span>Carrera 2 # 16A-62</span>
          </li>
          <!-- End li -->

          <li v-scroll-reveal="{ delay: 60, distance: '20px' }">
            <span><a href="#">yesidvh@gmail.com</a></span>
            <span>+57 3115944439</span>
          </li>
          <!-- End li -->

          <li v-scroll-reveal="{ delay: 80, distance: '20px' }">
            <div class="social">
              <ul>
                <li v-for="(social, i) in socialList" :key="i">
                  <a :href="social.link" target="_blank">
                    <span class="first"
                      ><img class="svg" :src="social.icon" alt="social icon"
                    /></span>
                    <span class="second"
                      ><img class="svg" :src="social.icon" alt="social icon"
                    /></span>
                  </a>
                </li>
              </ul>
            </div>
          </li>
        </ul>
      </div>
      <!-- End .copyright_inner -->
    </div>
    <!-- End .container -->
  </div>
  <!-- End .waxon_tm_copyright -->
</template>

<script>
export default {
  data() {
    return {
      socialList: [
        {
          icon: require("../assets/img/svg/social/facebook.svg"),
          link: "https://www.facebook.com/",
        },
        {
          icon: require("../assets/img/svg/social/twitter.svg"),
          link: "https://twitter.com/yesidvh",
        },
        {
          icon: require("../assets/img/svg/social/instagram.svg"),
          link: "https://www.instagram.com/yesidvh",
        },
        {
          icon: require("../assets/img/svg/social/linkedin.svg"),
          link: "https://www.linkedin.com/in/yesid-valenzuela-57b0ba3b/",
        },
        {
          icon: require("../assets/img/svg/social/youtube.svg"),
          link: "youtube.com/channel/UC8ipUz9xUTQg4ApmY-yRqJQ/featured",
        },
        {
          icon: require("../assets/img/svg/social/tik-tok.svg"),
          link: "https://www.tiktok.com/@viviendoes",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
