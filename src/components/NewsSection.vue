import axios from 'axios'
<template>
    <div>
        <div class="row row-cols-1 row-cols-md-2">
            <div class="col mb-3 mt-3" v-for="(movie, index) of movies" :key= "index">
                <div class="card mb-3" style="max-width: 540px;">
                    <div class="row no-gutters">
                        <div class="col-md-4">
                            <img v-bind:src="movie.Poster" class="card-img" alt="...">
                        </div>
                        <div class="col-md-8">
                            <div class="card-body">
                                <h5 class="card-title">{{movie.Title}}</h5>
                                <p class="card-text">This is a wider card with supporting text below as a natural lead-in to additional content. This content is a little bit longer.</p>
                                <a v-bind:href="'https://www.imdb.com/title/' + movie.imdbID" target="_blank" class="btn btn-primary">Ver más</a>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'NewsSection',
    data() {
        return{
            movies: null
        }
    },

    mounted() {

        this.$axios.
        get('http://www.omdbapi.com/?s=harry+potter&type=movie&apikey=23daade9')
        .then(response => {
            (this.movies = response.data.Search.slice(0,4))
            console.log(this.movies)
        })
    },


}

</script>

<style>

</style>