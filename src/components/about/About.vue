<template>
  <div class="waxon_tm_about" id="about">
    <div class="container">
      <div class="about_inner">
        <div class="left" v-scroll-reveal="{ delay: 40 }">
          <img
            class="thumbnail"
            src="../../assets/img/about/yesid.jpg"
            alt="man with sunglass"
          />
        </div>
        <!-- End left thumbnail -->
        <div class="right">
          <div class="name" v-scroll-reveal="{ delay: 40 }">
            <h3>Yesid Valenzuela Hoyos<span class="bg">SobreMí</span></h3>
            <span class="job"
              >Ingeniero de sistemas &amp; Especialista en Marketing</span
            >
          </div>
          <div class="text">
            <p v-scroll-reveal="{ delay: 60 }">
              Amo la vida y con ella todo lo que hago. Tengo hobbies que me
              permiten vivir la vida plenamente, soy una persona proactiva con
              habilidad en manejo de grupos, fluidez verbal en español e ingles.
            </p>
            <p v-scroll-reveal="{ delay: 80 }">
              Utilizo los conocimientos de sistemas y marketing para
              diagnosticar, construir, evaluar y hacer crecer las organizaciones
              obteniendo el maximo beneficio.
            </p>
          </div>
          <div class="waxon_tm_button" v-scroll-reveal="{ delay: 100 }">
            <button class="ib-button" @click="showModal">
              <span>Ver mas</span>
            </button>
          </div>
        </div>
        <!-- End right content -->
      </div>
    </div>

    <!-- Start Modalbox -->
    <transition name="fade">
      <!-- Modal -->
      <div
        :class="{ 'modal-mask': isActive }"
        id="modal"
        @click="closeModal"
        v-if="isVisible"
      >
        <div
          class="
            modal-dialog
            modal-dialog-centered
            modal-dialog-scrollable
            modal-user
          "
          @click.stop
        >
          <div class="modal-content">
            <div class="waxon_tm_modalbox_about">
              <div class="close" @click="closeModal">
                <img
                  class="svg"
                  src="../../assets/img/svg/cancel.svg"
                  alt="cancel-img"
                />
              </div>
              <!-- End .close -->
              <div class="my_box">
                <div class="left">
                  <div class="about_title">
                    <h3>Habilidades</h3>
                  </div>
                  <!-- End .abut_title -->
                  <div class="waxon_progress">
                    <div class="progress_inner">
                      <span><span class="label">Base de datos</span> </span>
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span><span class="label">Google Analytics</span></span>
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span><span class="label">Ads</span></span>
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                  </div>
                  <!-- End .waxon_progress -->
                </div>
                <!-- End .left -->
                <div class="right">
                  <div class="about_title">
                    <h3>Idiomas</h3>
                  </div>
                  <div class="waxon_progress">
                    <div class="progress_inner">
                      <span><span class="label">Español</span></span>
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                    <div class="progress_inner">
                      <span><span class="label">Ingles</span></span>
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- End .right -->
              </div>
              <div class="grafica">
                <figure class="pie-chart">
                  <h2 class="job">Mis Fortalezas</h2>
                  <figcaption>
                    Creatividad 20<span style="color: #337ac7"></span><br />
                    Trabajo en equipo 30<span style="color: #95bcda"></span
                    ><br />
                    Trabajo bajo presión 20<span style="color: #e3e647"></span
                    ><br />
                    Analisis de información 30<span
                      style="color: #023f79"
                    ></span>
                  </figcaption>
                </figure>
              </div>
              <!-- <div class="counter">
                <div class="about_title">
                  <h3>Fun Facts</h3>
                </div>
                <ul>
                  <li>
                    <div class="list_inner">
                      <h3>777+</h3>
                      <span>Projects Completed</span>
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <h3>3K</h3>
                      <span>Happy Clients</span>
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <h3>9K+</h3>
                      <span>Lines of Code</span>
                    </div>
                  </li>
                </ul>
                
              </div> -->

              <!-- End .counter -->
              <!-- <div class="partners">
                <div class="about_title">
                  <h3>Our Partners</h3>
                </div>
                <Brand />
              </div> -->
              <!-- End .partner -->
            </div>
            <!-- End .tokyo_tm_modalbox_about -->
          </div>
        </div>
      </div>
    </transition>
    <!-- End Modalbox -->
  </div>
  <!-- End about -->
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      isVisible: false,
    };
  },
  methods: {
    showModal: function () {
      this.isActive = true;
      this.isVisible = true;
    },
    closeModal: function () {
      this.isActive = false;
      this.isVisible = false;
    },
  },
};
</script>
<style scoped>
.grafica {
  text-align: center;
  margin: 0 auto;
}
.pie-chart {
  background: radial-gradient(
      circle closest-side,
      white 0,
      white 48%,
      transparent 48%,
      transparent 64%,
      white 0
    ),
    conic-gradient(
      from 50deg,
      #337ac7 0,
      #337ac7 20%,
      #95bcda 0,
      #95bcda 50%,
      #e3e647 0,
      #e3e647 70%,
      #023f79 0,
      #023f79 100%
    );
  position: relative;
  width: 60%;
  min-height: 350px;
  margin: 2rem auto 0;
  outline: 1px solid #ccc;
}
.pie-chart figcaption {
  position: absolute;
  bottom: 1em;
  right: 1em;
  font-size: smaller;
  text-align: right;
}
.pie-chart span:after {
  display: inline-block;
  content: "";
  width: 0.8em;
  height: 0.8em;
  margin-left: 0.4em;
  height: 0.8em;
  border-radius: 0.2em;
  background: currentColor;
}
@media screen and (max-width: 900px) {
  .pie-chart {
    width: 80%;
    min-height: 450px;
  }
}
</style>
