<template>
  <div class="general">
    <div class="center">
      <section id="content">
        <h1 class="subheader">Peliculas</h1>
        La Pelicula favorita es:
        <h2>{{favorita.tittle}}</h2>
        <!--Listado articulos-->
        <div id="articles">
          <!-- v-for="pelicula in peliculas" v-bind:key="pelicula.tittle" -->

          <!--AÑADIR ARTICULOS VIA JS-->
          <div v-for="pelicula in peliculas" v-bind:key="pelicula.tittle">
            <Pelicula 
              :pelicula="pelicula"
              v-on:favorita="haLlegadoLaPeliculaFavorita"
              ></Pelicula>
          </div>
        </div>
      </section>
      <Sidebar></Sidebar>

      <div class="clearfix"></div>
    </div>
  </div>
</template>

<script>
import Sidebar from "./Sidebar.vue";
import Pelicula from "./Pelicula.vue";

export default {
  name: "Peliculas",
  components: {
    Pelicula,
    Sidebar,
  },
  methods:{
    haLlegadoLaPeliculaFavorita(favorita){
      this.favorita = favorita;
      
    }
  },
  data() {
    return {
      favorita : null,
      peliculas: [
        {
          tittle: "Batman",
          year: 2017,
          image:
            "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRUGNnaP0TgldPUGceJDZKvEti-DSuUErJkhZSQC6pwLjYjIYPdNHV_BMFBIx6n4_0rnoI&usqp=CAU",
        },
        {
          tittle: "Superman",
          year: 2020,
          image:
            "https://imagenes.20minutos.es/files/article_amp/uploads/imagenes/2021/03/23/henry-cavill-como-superman.jpeg",
        },
        {
          tittle: "ironman",
          year: 2021,
          image:
            "https://cdn-e360.s3-sa-east-1.amazonaws.com/adios-robert-downey-jr-marvel-anuncio-al-nuevo-iron-man-large-UQ4lZe7Bcu.jpg",
        },
      ],
    };
  },
};
</script>