<template>
  <ParticleDemo />
  <!-- End wrapper all -->
</template>

<script>
import ParticleDemo from './all-home-version/ParticleDemo.vue';
export default {
  components:{
    ParticleDemo
  },
  data() {
    return {
      prevImg: require("../assets/img/intro/preview.jpg"),
    };
  },
  mounted() {
    document.body.classList.add("preview-page");
  },
  destroyed() {
    document.body.classList.remove("preview-page");
  },
};
</script>

<style lang="scss">
.preview-page .back-top {
  display: none;
}
</style>
