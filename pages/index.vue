<template>
  <div>
    <div>
      <div class="bg-[url('/public/bg.jpg')]">
        <div class="p-5">
          <navbar />

          <div class="text-white">
            <div class="mt-5 text-center font-poppins">Top 10 Movies</div>
            <div
              class="md:grid grid-cols-2 lg:grid-cols-3 xl:grid-cols-4"
            ></div>
          </div>
        </div>
        <div>
          <div class="grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
            <!-- object transfer -->
            <cart v-for="(item,index) in topMovies" :key="index" :item="item" /> 
          </div>
        </div>
        <div
          class="h-16 w-full bg-black text-white flex items-center justify-center"
        >
          TamilBlasters
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      topMovies: [
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
        {
          Title: "Leo",
          img: "/leo.jpg",
        },
      ],
    };
  },
};
</script>
