<template>
  <div class="bg-[url('/public/bg.jpg')] ">
    <div class="p-5">
      <navbar />

     <div class="text-white">
        <div class="mt-5 text-center font-poppins">Top 10 Movies</div>
        <div class="md:grid grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
          <div
            v-for="(list, index) in topMovies"
            class="grid items-center justify-center mt-5"
          >
            <img :src="list.img" alt="" />
            <p class="text-center">{{ list.Title }}</p>
          </div>
        </div>
     </div>
    </div>
    <div
      class="h-16 w-full bg-black text-white flex items-center justify-center"
    >
      TamilBlasters
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
