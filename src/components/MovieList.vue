<template>
  <div id="movie-container">MovieList
      <movie v-for="movie in movies" :key="movie.id" :movie="movie" />
  </div>
</template>

<script>
import Movie from './Movie'

export default {
    components: {
        Movie,
    },
    data() {
        return {
            movies: [],
        };
    },
    computed: {
        movies() {
            return this.$store.getters.getMovies;
        },
    },
//   created() {
//       this.movies = this.$store.getters.getMovies;      
//   }
};
</script>

<style lang='scss' scoped>
	#movie-container {
        color: #fff;
		padding-top: 1rem;
		display: flex;
		flex-wrap: wrap;
		flex-grow: 2;
		justify-content: center;
	}
</style>
