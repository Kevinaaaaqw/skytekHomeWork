<script setup lang="ts">
  import {movieList} from "./pinia"
  const movie = movieList().list
</script>

<template>
    <main>
      <router-link to="/" class="nav-link">電影</router-link>
      <div class="intro">this is cart</div>
      <div v-for="movie in movie" style="border:1px solid black;display:flex;justify-content:space-between">
        <div>
          <div>{{movie.Title}}</div>
          <div>{{movie.Year}}</div>
          <div>{{movie.Type}}</div>
          <div>{{movie.imdbID}}</div>
          </div>
          <img  :src="movie.Poster"/>
      </div>
    </main>
</template>

<style scoped></style>