<template>
  <div class="general">
    <Slider texto="Pagina"></Slider>
    <div class="center">
      <section id="content">
        <h2 class="subheader">Pagina de Prueba</h2>
        <h3>{{ id_desde_url }}</h3>
        <button @click="actualizarNombre()">Actualizar Nombre</button>
        <button @click="RedirigirBlog()">Redirigir</button>
        <h4>{{ nombre }}</h4>
      </section>
      <Sidebar></Sidebar>

      <div class="clearfix"></div>
    </div>
  </div>
</template>
<script>
import Slider from "./Slider.vue";
import Sidebar from "./Sidebar.vue";
export default {
  name: "Pagina",
  created() {
    console.log("componente creado");
  },
  mounted() {
    this.id_desde_url = this.$route.params.id;
    console.log("componente montado");
  },
  updated() {
    console.log("componente actualizado");
  },
  destroyed() {
    console.log("componente eliminado");
  },
  data() {
    return {
      id_desde_url: null,
      nombre: "Victor",
    };
  },
  methods: {
    actualizarNombre() {
      this.nombre = "VICTOR ZAMORA";
      console.log(this.nombre);
    },
    RedirigirBlog() {
      this.$router.push("/blog");
    },
  },
  components: {
    Slider,
    Sidebar,
  },
};
</script>