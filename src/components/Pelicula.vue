<template>
  
      <article class="article-item">
        <div class="image-wrap">
          <img
            :src="pelicula.image"
            :alt="pelicula.tittle"
            :title="pelicula.tittle"
          />
        </div>

        <h2>{{ pelicula.tittle }}</h2>
        <span
          class="date"
          v-bind:class="{
            yeargreen: pelicula.year >= 2020,
            yearblue: pelicula.year < 2020,
          }"
        >
          {{ pelicula.year }}
        </span>
        <a href="#">Leer más</a>
        <input type="button" value="Marcar como favorito" 
        @click="pasarFavoritaAlPadre(pelicula)"
        />

        <div class="clearfix"></div>
      </article>
      
</template>
<script>


export default {
  name: "Pelicula",
  props: ["pelicula"],
  methods: {
    pasarFavoritaAlPadre(pelicula){
      console.log(pelicula);
      this.$emit('favorita', pelicula);
    }
  }
  
};

</script>