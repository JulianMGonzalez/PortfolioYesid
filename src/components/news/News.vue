<template>
  <div class="news_inner">
    <div class="linea-tiempo">
      <div class="momento">
        <h3>Cootranshuila Ltda</h3>
        <p>Líder de Recursos Humanos y Marketing</p>
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
      <div class="momento">
        <h3>Amazonia y Consultoría S.A.S</h3>
        <p>Asesor de Marketing & Tecnología</p>
        <div class="descripcion">
          Creacion de Marca, Manejo de la imagen corporativa y consultoría en
          Tecnología.<br /><br /><br />
        </div>
      </div>
      <div class="momento">
        <h3>
          Universidad Corporación unificada nacional de educación superior
        </h3>
        <p>Coordinador de Educación Continua</p>
        <div class="descripcion">
          Docente de un diploma como opción de Grado para estudiantes de
          Comunicación Social. El Diplomado fue en Comunity Management de 120
          Horas. 22 Estudiantes. Curso dictado sábados y medio Día Domingo.
          <br /><br />
        </div>
      </div>
      <div class="momento">
        <h3>FOODSTORE</h3>
        <p>Kitchen Porter Manager</p>
        <div class="descripcion">
          Trabajar con el empleador para garantizar la operación exitosa y
          rentable de su establecimiento. Promover los intereses del empleador ,
          desarrollar y mantener un ambiente de trabajo donde hay mutua
          confianza y cooperación entre el empleado y el empleador .
          Proporcionar puntual y completa información a la Chef Ejecutivo y
          Gerente General
        </div>
      </div>
      <div class="momento">
        <h3>Cooptenjo Entidad Cooperativa de Ahorro y Crédito</h3>
        <p>Coordinador de T.I</p>
        <div class="descripcion">
          ✓ Manejo de Proveedores de Comunicaciones<br />
          ✓ Creación e Implementación Proyecto de VoIP en Asterisk. <br />
          ✓ Apoyo en General a la Dirección de T.I <br />
          ✓ Revisión y evaluación de las redes (LAN, WAN) <br />
          ✓ Administración del Centro de Datos.
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
@media screen and (max-width: 768px) {
  .momento h3{
    font-size: 20px;
  }
}
</style>
