<template>
  <section id="content">
    <div id="mi-componente">
      <hr />
      <h1>Este es mi componente</h1>
      <h2>{{ subtitulo }}</h2>
      <hr />

      <h2>Reactividad</h2>
      <input type="text" v-model="nombre" />
      Mi nombre es: <strong>{{ nombre }}</strong>

      <h2>Directivas Condicionales</h2>
      <input type="number" v-model="edad" />
      Mi edad es <strong>{{ edad }}</strong>

      <p style="color: red; font-weigth: bold" v-if="edad && edad >= 18 && edad <60">
        Eres mayor de edad
      </p>
      <p style="color: green; font-weigth: bold" v-else-if="edad && edad >= 60">
        Eres de tercera de edad
      </p>

      <p style="color: blue; font-weigth: bold" v-else>
        Eres menor de edad
      </p>

      <h2>Directiva iterativas</h2>
      <ol>
          <li v-for="pelicula in peliculas" :key="pelicula">{{pelicula}}</li>
      </ol>
    </div>
  </section>
</template>

<script>
export default {
  name: "MiComponente",
  data() {
    return {
      subtitulo: "Soy el subtitulo de mi componente",
      nombre: "",
      edad: "",
      peliculas : ['batman', 'superman', 'spiderman', 'ironman']
    };
  },
};
</script>
