<template>
  <!-- HERO -->
  <div class="waxon_tm_hero" id="home">
    <div class="background">
      <div class="leftpart"></div>
      <div class="rightpart">
        <div class="inner">
          <vue-particles
            color="#bbb"
            :particleOpacity="0.7"
            :particlesNumber="30"
            shapeType="circle"
            :particleSize="5"
            linesColor="#777"
            :linesWidth="1"
            :lineLinked="true"
            :lineOpacity="0.4"
            :linesDistance="180"
            :moveSpeed="6"
            :hoverEffect="true"
            hoverMode="repulse"
            :clickEffect="false"
            clickMode="push"
          >
          </vue-particles>
          <div
            class="image"
            :style="{ backgroundImage: 'url(' + sliderHero + ')' }"
          ></div>
          <div class="overlay_image"></div>
          <div class="myOverlay"></div>
        </div>
      </div>
    </div>
    <div class="content">
      <div class="container">
        <div class="content_inner">
         <div class="name">
            <h3 class="stroke" v-scroll-reveal="{ delay: 1000 }">
              Yesid
            </h3>
            <h3 v-scroll-reveal="{ delay: 1050 }">Valenzuela</h3>
            <span v-scroll-reveal="{ delay: 1100 }"
              >Ingeniero de sistemas &amp; Especialista en Marketing</span
            >
          </div>
        </div>
        <div class="waxon_tm_down" data-skin="dark">
          <div class="line_wrapper">
            <div class="line"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!-- /HERO -->
</template>

<script>
export default {
  data() {
    return {
      sliderHero: require("../../assets/img/intro/marketing.jpg"),
    };
  },
};
</script>

<style lang="scss" >
#particles-js {
  z-index: 5;
}
</style>
