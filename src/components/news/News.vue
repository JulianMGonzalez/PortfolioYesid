<template>
  <div class="news_inner">
    <div class="linea-tiempo">
      <div class="momento">
        <h3>Marketing - EOI Madrid España</h3>
        <p>2008-2009</p>
        <div class="descripcion"><br><br><br></div>
      </div>
      <div class="momento">
        <h3>Management - New Zealand</h3>
        <p>2010-2014</p>
        <div class="descripcion">Innstitute of Management National<br><br><br></div>
      </div>
      <div class="momento">
        <h3>Bambuquero</h3>
        <p>2014-2015</p>
        <div class="descripcion">Baloncesto Profesional<br><br><br></div>
      </div>
      <div class="momento">
        <h3>Lider de Tecnologia y Marketing</h3>
        <p>2016-2022</p>
        <div class="descripcion">
          Responsable por mantener en perfectas y continuas actualizaciones
          todos los niveles de información de la Compañía, disponibles para ser
          analizadas. Aprovechando el manejo de la esta, obteniendo el máximo de
          beneficio para generar campañas de Marketing que permita el
          posicionamiento y fortalecimiento de la Marca, haciendo mas fuerte y
          competitivos dentro del entorno, dando el máximo de beneficio tanto al
          Cliente y Asociado de la Empresa.
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      isActive: false,
      isActive2: false,
      isActive3: false,
      isVisible: false,
      isVisible2: false,
      isVisible3: false,
      imgSrc: require("../../assets/img/news/1.jpg"),
      imgSrc2: require("../../assets/img/news/2.jpg"),
      imgSrc3: require("../../assets/img/news/3.jpg"),
    };
  },
};
</script>

<style lang="scss" scoped>
.linea-tiempo {
  position: relative;
  width: 100%;
  max-width: 95vw;
  height: 100%;
  font-family: Arial;
}

.linea-tiempo::before {
  content: "";
  position: absolute;
  width: 3px;
  background-color: #000;
  left: 50%;
  height: 100%;
  border-radius: 10px;
}

.momento {
  position: relative;
  width: 45%;
  box-sizing: border-box;
}

.momento:nth-child(even) {
  left: 55%;
}

.momento::after {
  content: "";
  position: absolute;
  top: calc(50% + 10px);
  right: calc(-11.11% - 11.5px);
  height: 20px;
  width: 20px;
  background-color: #000;
  border-radius: 50%;
}

.momento:nth-child(even)::after {
  left: calc(-11.11% - 8.5px);
}

.momento h3 {
  margin: 10px 0px;
  font-size: 30px;
  text-align: center;
}
.momento p {
  text-align: center;
}

.momento .descripcion {
  background-color: #eee;
  border-radius: 10px;
  padding: 10px;
  line-height: 22px;
  font-size: 14px;
}

.momento .descripcion::after {
  content: "";
  position: absolute;
  right: -10px;
  top: calc(50% + 10px);
  height: 0;
  width: 0;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-left: 12px solid #eee;
}

.momento:nth-child(even) .descripcion {
  background-color: #3393fe;
  color: white;
}

.momento:nth-child(even) .descripcion::after {
  left: -10px;
  border-top: 10px solid transparent;
  border-bottom: 10px solid transparent;
  border-right: 12px solid #3393fe;
  border-left: none;
}
</style>
