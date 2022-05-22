<template>
  <div class="waxon_tm_about" id="about">
    <div class="container">
      <div class="about_inner">
        <div class="left" v-scroll-reveal="{ delay: 40 }">
          <img
            class="thumbnail"
            src="../../assets/img/about/2.jpg"
            alt="man with sunglass"
          />
        </div>
        <!-- End left thumbnail -->
        <div class="right">
          <div class="name" v-scroll-reveal="{ delay: 40 }">
            <h3>Yesid Valenzuela Hoyos<span class="bg">About</span></h3>
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
                    <h3>Photography Skills</h3>
                  </div>
                  <!-- End .abut_title -->
                  <div class="waxon_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">Base de datos </span
                        ><span class="number">95%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 95%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">Google Analytics</span
                        ><span class="number">90%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 90%"></div>
                        </div>
                      </div>
                    </div>
                    <!-- End progress_inner -->
                    <div class="progress_inner">
                      <span
                        ><span class="label">Ads</span
                        ><span class="number">90%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 90%"></div>
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
                    <h3>Language Skills</h3>
                  </div>
                  <div class="waxon_progress">
                    <div class="progress_inner">
                      <span
                        ><span class="label">Español</span
                        ><span class="number">100%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 100%"></div>
                        </div>
                      </div>
                    </div>
                    <div class="progress_inner">
                      <span
                        ><span class="label">Ingles</span
                        ><span class="number">95%</span></span
                      >
                      <div class="background">
                        <div class="bar">
                          <div class="bar_in" style="width: 95%"></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- End .right -->
              </div>
              <div class="counter">
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
                <!-- End ul -->
              </div>
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
  components: {
  },
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
