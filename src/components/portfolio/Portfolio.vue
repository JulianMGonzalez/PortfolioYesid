<template>
  <div class="container">
    <div
      class="positon-relative waxon_tm_main_title"
      v-scroll-reveal="{ delay: 40, distance: '30px' }"
    >
      <div class="title">
        <h3>Logros<span class="bg">Portafolio</span></h3>
      </div>
      <!-- End shane_tm_title -->
      <div class="portfolio_filter" :class="{ opened: active }">
        <ul>
          <li>
            <a
              v-on:click="activetab = 1"
              :class="[activetab === 1 ? 'current' : '']"
              ><span class="first">All</span> <span class="second">Todo</span></a
            >
          </li>
          <!-- End All for tabcontent 1 -->
          <!-- End Vimeo tabcontent 2 -->
          <li>
            <a
              v-on:click="activetab = 3"
              :class="[activetab === 3 ? 'current' : '']"
              ><span class="first">Youtube</span>
              <span class="second">Youtube</span></a
            >
          </li>
          <!-- End .Youtube tabcontent 3 -->
          <li>
            <a
              v-on:click="activetab = 4"
              :class="[activetab === 4 ? 'current' : '']"
              ><span class="first">Imagenes</span>
              <span class="second">Imagenes</span></a
            >
          </li>
          <!-- End Mix tabcontent 4 -->
        </ul>
        <div
          class="wrapper"
          @click="active = !active"
          :aria-pressed="active ? 'true' : 'false'"
        >
          <span class="trigger"></span>
        </div>
      </div>
      <!-- End .portfolio-filter -->
    </div>

    <div v-if="activetab === 1" class="tabcontent">
      <div class="portfolio_inner">
        <ul>
          <CoolLightBox :items="allItems" :index="index" @close="index = null">
          </CoolLightBox>
          <li v-for="(image, imageIndex) in allItems" :key="imageIndex">
            <div class="list_inner">
              <div class="image" @click="index = imageIndex">
                <img src="../../assets/img/thumbs/1-1.jpg" alt="Portfolio" width="100%"/>
                <div
                  class="main"
                  :style="{ backgroundImage: 'url(' + image.thumb + ')' }"
                ></div>
              </div>
              <!-- End .image -->
              <div class="title">
                <h3 @click="index = imageIndex">{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
      </div>

      <!-- End .portfolio_list -->
    </div>
    <!-- End All .tabcontent 1 -->

    <!-- End Vimeo .tabcontent 2 -->

    <div v-if="activetab === 3" class="tabcontent">
      <div class="portfolio_inner">
        <ul>
          <CoolLightBox
            :items="youtubeItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>
          <li v-for="(image, imageIndex) in youtubeItems" :key="imageIndex">
            <div class="list_inner">
              <div class="image">
                <img src="../../assets/img/thumbs/1-1.jpg" alt="Portfolio" />
                <div
                  class="main"
                  @click="index = imageIndex"
                  :style="{ backgroundImage: 'url(' + image.thumb + ')' }"
                ></div>
              </div>
              <!-- End .image -->
              <div class="title">
                <h3 @click="index = imageIndex">{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End Youtube .tabcontent 3 -->

    <div v-if="activetab === 4" class="tabcontent">
      <div class="portfolio_inner">
        <ul>
          <CoolLightBox
            :items="galleryItems"
            :index="index"
            @close="index = null"
          >
          </CoolLightBox>

          <li v-for="(image, imageIndex) in galleryItems" :key="imageIndex">
            <div class="list_inner">
              <div class="image">
                <img src="../../assets/img/thumbs/1-1.jpg" alt="Portfolio" />
                <div
                  class="main"
                  @click="index = imageIndex"
                  :style="{ backgroundImage: 'url(' + image.thumb + ')' }"
                ></div>
              </div>
              <!-- End .image -->
              <div class="title">
                <h3 @click="index = imageIndex">{{ image.portfolioName }}</h3>
                <span>{{ image.portfolioType }}</span>
              </div>
            </div>
          </li>
          <!-- End li -->
        </ul>
        <!-- End .portfolio_list -->
      </div>
    </div>
    <!-- End Image .tabcontent 4 -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: false,
      activetab: 1,
      allItems: [
        {
          src: "https://youtu.be/r_2ke3u1Fvk",
          thumb: require("../../assets/img/portfolio/pitalito.png"),
          portfolioName: "Proyecto para la alcaldia de Pitalito",
          portfolioType: "Youtube",
        },
        {
          src: require("../../assets/img/portfolio/primerafondo.jpeg"),
          thumb: require("../../assets/img/portfolio/primera.jpeg"),
          portfolioName: "Ser la Primera empresa de Transporte en el Huila Certificada por competencias a los Conductores",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/diplomado.jpeg"),
          thumb: require("../../assets/img/portfolio/diplomadofondo.jpeg"),
          portfolioName: "Profesor en Diplomado a Estudiantes como opción de grado para los comunicadores sociales: 'Diplomado en Community Management' Neiva. Universidad CUN",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/china.jpeg"),
          thumb: require("../../assets/img/portfolio/chinafondo.jpeg"),
          portfolioName: "Visita a China para implementación de proyectos de cámaras a buses y nuevas unidades de Negocios",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/saludablefondo.jpeg"),
          thumb: require("../..//assets/img/portfolio/saludable.jpeg"),
          portfolioName: "Se han creado campañas de concientización de hábitos saludables.",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/capacitacion.jpeg"),
          thumb: require("../..//assets/img/portfolio/capacitacionfondo.jpeg"),
          portfolioName: "Capacitaciones al Personal en Servicio al Cliente, Liderazgo y motivacion.",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/posicionamiento.jpeg"),
          thumb: require("../..//assets/img/portfolio/posicionamientofondo.jpeg"),
          portfolioName: "Refrescar la Marca y posicionamiento de cootranshuila.",
          portfolioType: "Gallery",
        },
      ],
      youtubeItems: [
        {
          src: "https://youtu.be/r_2ke3u1Fvk",
          thumb: require("../../assets/img/portfolio/pitalito.png"),
          portfolioName: "Proyecto para la alcaldia de Pitalito",
          portfolioType: "Youtube",
        },
      ],
      galleryItems: [
        {
          src: require("../../assets/img/portfolio/primerafondo.jpeg"),
          thumb: require("../../assets/img/portfolio/primera.jpeg"),
          portfolioName: "Ser la Primera empresa de Transporte en el Huila Certificada por competencias a los Conductores",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/diplomado.jpeg"),
          thumb: require("../../assets/img/portfolio/diplomadofondo.jpeg"),
          portfolioName: "Profesor en Diplomado a Estudiantes como opción de grado para los comunicadores sociales: 'Diplomado en Community Management' Neiva. Universidad CUN",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/china.jpeg"),
          thumb: require("../../assets/img/portfolio/chinafondo.jpeg"),
          portfolioName: "Visita a China para implementación de proyectos de cámaras a buses y nuevas unidades de Negocios",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/saludablefondo.jpeg"),
          thumb: require("../..//assets/img/portfolio/saludable.jpeg"),
          portfolioName: "Se han creado campañas de concientización de hábitos saludables.",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/capacitacion.jpeg"),
          thumb: require("../..//assets/img/portfolio/capacitacionfondo.jpeg"),
          portfolioName: "Capacitaciones al Personal en Servicio al Cliente, Liderazgo y motivacion.",
          portfolioType: "Gallery",
        },
        {
          src: require("../..//assets/img/portfolio/posicionamiento.jpeg"),
          thumb: require("../..//assets/img/portfolio/posicionamientofondo.jpeg"),
          portfolioName: "Refrescar la Marca y posicionamiento de cootranshuila.",
          portfolioType: "Gallery",
        },
      ],
      index: null,
    };
  },
};
</script>

<style lang="scss" scoped></style>
