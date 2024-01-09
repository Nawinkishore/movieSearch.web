<template>
  <div>
    <div>
      <div class="h-full w-full bg-[#e5e5e5]">
        <div class="bg-[url('/public/bg.jpg')] h-screen">
          <div class="flex w-full">
            <div class="flex items-center gap-3 p-3">
              <NuxtLink to="/explore">
                <i
                  class="fa-solid fa-chevron-left cursor-pointer text-white hover:text-blue-500"
                ></i>
              </NuxtLink>
            </div>
            <div class="p-5 w-full">
              <navbar search="search" />
            </div>
          </div>

          <div
            class="!text-white flex flex-col items-start justify-start mt-5 p-3"
          >
            <div><img :src="redirectMovie[0].img" alt="" /></div>
            <div class="font-bold">{{ redirectMovie[0].Title }}</div>
            <div>Director : {{ redirectMovie[0].about[0].director }}</div>
            <div>Writers : {{ redirectMovie[0].about[0].Writers }}</div>
            <div class="flex flex-row mt-2">
              <button
                v-for="(gen, index) in redirectMovie[0].genre"
                :key="index"
                class="mr-2 bg-blue-500 text-white p-2 rounded-md"
              >
                {{ gen }}
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      search: false,
      redirectMovie: [
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
      ],
    };
  },
};
</script>
