<template>
  <div id="movie-container">MovieList
      <ul>
          <li v-for="(movie, index) in movies" :key="movie.id">
              Index: {{ index }} {{ movie.name }}
              </li>
      </ul>
  </div>
</template>

<script>
export default {
  data() {
      return {
          movies: [
              {id: 1,
              name: 'movie-1'},
              {id: 2,
              name: 'movie-2'},
              {id: 3,
              name: 'movie-3'},
          ]
      }
  }
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
