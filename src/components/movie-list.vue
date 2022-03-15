<template>
  <div class="container mx-auto">
    <div class="border-b py-8 border-gray-300" v-for="movie of movies" :key="movie.id">
      <div class="flex items-start">
        <div class="mr-4 relative">
            <img :src="movie.img" alt="" />
            <img class="mustsee_movie" v-if="movie.mustsee === true" src="https://www.metacritic.com/images/icons/mc-mustsee-sm.svg" alt="">
        </div>
        <div class="block w-full">
          <h2 class="text-xl font-semibold">
            {{ movie.id }}. {{ movie.title }}
          </h2>
          <p class="my-2 text-gray-400">{{ movie.date }}</p>
          <p>{{ movie.desc }}</p>
        </div>
        <p class="bg-green-400 text-white text-xl font-semibold p-3 rounded-md">
          {{ movie.rate }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      movies: [],
      baseURL: "",
    };
  },
  async mounted() {
    try {
      const res = await axios.get(`http://localhost:3001/movies`);
      this.movies = res.data;
      console.log(res);
    } catch (e) {
      console.error(e);
    }
  },
};
</script>