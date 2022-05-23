<template>
  <!-- SERVICES -->
  <div class="waxon_tm_service">
    <div class="container">
      <div class="service_inner">
        <ul>
          <hooper :settings="hooperSettings">
            <slide v-for="(service, i) in serviceContent" :key="i">
              <div class="list_inner">
                <img class="svg" :src="service.imgSrc" alt="service image" />
                <div class="details">
                  <h3>{{ service.title }}</h3>
                  <p>
                    {{ service.desc }}
                  </p>
                </div>
              </div>

              <!-- End item -->
            </slide>
          </hooper>
        </ul>
      </div>
    </div>
  </div>
  <!-- /SERVICES -->
</template>

<script>
import { Hooper, Slide } from "hooper";
import "hooper/dist/hooper.css";
export default {
  components: {
    Hooper,
    Slide,
  },
  data() {
    return {
      serviceContent: [
        {
          imgSrc: require("../../assets/img/svg/bycicle.svg"),
          title: "MTB",
          desc: `Mi experiencia en el mundo de la montaña es una de las más importantes en la vida de una persona.`,
        },
        {
          imgSrc: require("../../assets/img/svg/nature.svg"),
          title: "Naturaleza",
          desc: `La naturaleza es una de las cosas más importantes en mi vida.`,
        },
        {
          imgSrc: require("../../assets/img/svg/cooking.svg"),
          title: "Cooking",
          desc: `Me gusta mucho la cocina, porque es una de las cosas que me hacen sentir más cómodo.`,
        },
        {
          imgSrc: require("../../assets/img/svg/reader.svg"),
          title: "Lectura",
          desc: `Participo en muchas actividades de lectura, porque es una de las cosas que me hacen sentir más cómodo.`,
        },
      ],
      hooperSettings: {
        infiniteScroll: true,
        wheelControl: false,
        autoPlay: false,
        mouseDrag: true,
        transition: 800,
        playSpeed: 1500,
        breakpoints: {
          1200: {
            itemsToShow: 3,
          },
          576: {
            itemsToShow: 2,
          },
          280: {
            itemsToShow: 1,
          },
        },
      },
    };
  },
};
</script>

<style lang="scss">
.service_inner {
  .hooper-slide {
    padding-right: 44px;
  }
}
</style>
