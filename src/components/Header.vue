<template>
  <div>
    <!-- TOPBAR -->
    <scroll-fixed-header :fixed.sync="fixed" :threshold="56">
      <div class="waxon_tm_topbar">
        <div class="container">
          <div class="topbar_inner">
            <div class="logo">
              <router-link to="/">
                <img src="../assets/img/logo/logo2.png" width="60px" alt="partners brand" />
              </router-link>
            </div>
            <div class="menu">
              <div class="links">
                <ul class="anchor_nav">
                  <scrollactive
                    bezier-easing-value=".5,0,.35,1"
                    :offset="69"
                    :duration="100"
                    :alwaysTrack="true"
                  >
                    <li class="current">
                      <a href="#home" class="scrollactive-item">
                        <span class="first">Inicio</span>
                        <span class="second">Inicio</span>
                      </a>
                    </li>
                    <li>
                      <a href="#about" class="scrollactive-item">
                        <span class="first">Sobre mí</span>
                        <span class="second">Sobre mí</span>
                      </a>
                    </li>
                    <li>
                      <a href="#portfolio" class="scrollactive-item">
                        <span class="first">Logros</span>
                        <span class="second">Logros</span>
                      </a>
                    </li>
                    <li>
                      <a href="#ultimo-años" class="scrollactive-item">
                        <span class="first">Ultimos Años</span>
                        <span class="second">Ultimos Años</span>
                      </a>
                    </li>
                    <li>
                      <a href="#contact" class="scrollactive-item">
                        <span class="first">Contacto</span>
                        <span class="second">Contacto</span>
                      </a>
                    </li>
                  </scrollactive>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
    </scroll-fixed-header>
    <!-- /TOPBAR -->

    <!-- MOBILE MENU -->
    <div class="waxon_tm_mobile_menu">
      <div class="topbar_inner">
        <div class="container bigger">
          <div class="topbar_in">
            <div class="logo">
              <router-link to="/">
                <img src="../assets/img/logo/logo2.png" alt="partners brand" />
              </router-link>
            </div>
            <div class="my_trigger">
              <div
                class="hamburger hamburger--collapse-r"
                :class="{ 'is-active': active }"
              >
                <div
                  class="hamburger-box"
                  @click="active = !active"
                  :aria-pressed="active ? 'true' : 'false'"
                >
                  <div class="hamburger-inner"></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div
        class="dropdown"
        :class="{ active: active }"
        :style="{ backgroundImage: 'url(' + pattern + ')' }"
      >
        <div class="container">
          <span
            class="close_menu"
            @click="active = !active"
            :aria-pressed="active ? 'true' : 'false'"
          >
            <img src="../assets/img/close.svg" alt="close menu" />
          </span>
          <div class="dropdown_inner">
            <ul class="anchor_nav">
              <scrollactive
                bezier-easing-value=".5,0,.35,1"
                :offset="76"
                :duration="100"
                :alwaysTrack="true"
              >
                <li>
                  <a
                    href="#home"
                    class="scrollactive-item"
                    @click="active = !active"
                    >Inicio</a
                  >
                </li>
                <li>
                  <a
                    href="#about"
                    class="scrollactive-item"
                    @click="active = !active"
                    >Sobre mi</a
                  >
                </li>
                <li>
                  <a
                    href="#portfolio"
                    class="scrollactive-item"
                    @click="active = !active"
                    >Portafolio</a
                  >
                </li>
                <li>
                  <a
                    href="#ultimo-años"
                    class="scrollactive-item"
                    @click="active = !active"
                    >Últimos años</a
                  >
                </li>
                <li>
                  <a
                    href="#contact"
                    class="scrollactive-item"
                    @click="active = !active"
                    >Contacto</a
                  >
                </li>
              </scrollactive>
            </ul>
            <div class="mobile-social">
              <Social />
            </div>
            <!-- End social share -->
          </div>
        </div>
      </div>
    </div>
    <!-- /MOBILE MENU -->
  </div>
</template>

<script>
import Social from "../components/Social.vue";
export default {
  components: {
    Social,
  },
  data() {
    return {
      active: false,
      fixed: false,
      pattern: require("../assets/img/patterns/1.png"),
    };
  },
};
</script>

<style lang="scss" scoped></style>
