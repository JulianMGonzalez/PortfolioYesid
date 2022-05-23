<template>
  <div class="waxon_tm_copyright">
    <div class="container">
      <div class="copyright_inner">
        <ul>
          <li>
            <span>Yesid Valenzuela &copy; {{ new Date().getFullYear() }}</span>
          </li>
          <!-- End li -->

          <li>
            <span>Neiva, Huila</span>
            <span>Carrera 2 # 16A-62</span>
          </li>
          <!-- End li -->

          <li>
            <span><a href="#">yesidvh@gmail.com</a></span>
            <span>+57 3115944439</span>
          </li>
          <!-- End li -->

          <li>
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
          link: "https://www.youtube.com/",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped></style>
