<template>
  <div class="select-none h-screen w-max-[768px]">
    <div class="h-screen w-full p-5">
      <div class="flex items-center gap-4">
        <NuxtLink to="/">
          <i class="fa-solid fa-house"></i>
        </NuxtLink>
        <h1 class="font-comforta-500">Explore New Movies</h1>
      </div>
      <div class="mt-5">
        <input
          type="search"
          placeholder="Search"
          class="border p-3"
          v-model="search"
          @keyup.enter="searchMovie"
        />
      </div>

      <!-- Top 10 movies -->
      <div>
        <div class="mt-5 font-comforta flex justify-start items-center gap-3">
          <h1>Top List Movies</h1>
          <i
            @click="showMovieList = !showMovieList"
            class="fa-solid"
            :class="{
              'fa-chevron-right': !showMovieList,
              'fa-chevron-down': showMovieList,
            }"
          ></i>
        </div>
      </div>
      <!-- Top movies -->
      <div
        v-if="showMovieList"
        class="grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4"
      >
        <div
          v-for="(list, index) in listMovies"
          :key="index"
          class="w-[200px] select-none"
        >
          <NuxtLink to="/detailsPage">
            <img
              @click="exploreRedirect(index)"
              :src="list.img"
              class="size-auto rounded-md mt-3 cursor-pointer hover:animate-pulse hover:shadow-md hover:shadow-slate-800"
            />
          </NuxtLink>
          <div class="flex items-center justify-between mt-3">
            <h1 class="font-semibold">{{ list.Title }}</h1>
            <p class="font-extralight">2023 . 2h 44m</p>
          </div>
        </div>
      </div>
    </div>
    <div v-if="showMovieList == false">
      <div
        class="h-16 w-full bg-black flex items-center justify-center text-white"
      >
        TamilBlasters
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      showMovieList: false,
      search: "",
      explore: false,
      redirectMovie: [],
      listMovies: [
        {
          Title: "Leo",
          img: "Leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "Hello",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },

        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
        {
          Title: "leo",
          img: "leo.jpg",
          about: [
            {
              director: "Lokesh Kanagaraj",
              Writers: "Lokesh Kanagaraj,Rathna Kumar,Deeraj Vaidy",
            },
          ],
          genre: ["Action", "Drama"],
        },
      ],
    };
  },
  methods: {
    exploreRedirect(index) {
      this.explore = true;
      this.redirectMovie = this.listMovies[index];
      this.search = "";
    },
    back() {
      this.explore = false;
      this.redirectMovie = "";
      this.search = "";
    },
    searchMovie() {
      const foundmovie = this.listMovies.find(
        (movie) => movie.Title.toLowerCase() === this.search.toLowerCase()
      );

      if (foundmovie) {
        alert("Movie founded");
      } else {
        alert("Movie is not founded");
      }
    },
  },
};
</script>
