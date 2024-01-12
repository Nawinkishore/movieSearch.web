<template>
  <div>
    <div
      class="flex items-center justify-between p-3 shadow-lg shadow-slate-600"
      :class="
        isTheme
          ? 'bg-[#440f6a] text-white rounded-lg'
          : 'bg-[#d4d4d8] rounded-lg'
      "
    >
      <div>{{ item }}</div>
      <div class="flex items-center gap-4">
        <i
          @click="isTheme = !isTheme"
          class="fa-solid fa-sun cursor-pointer"
        ></i>
        <NuxtLink to="/explore">
          <i
            class="fa-solid cursor-pointer"
            :class="search ? 'hidden' : 'fa-magnifying-glass'"
          ></i
        ></NuxtLink>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    item: {
      type: String,
      default: "TamilBlasters",
    },
    search: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {
      isTheme: false,
    };
  },
};
</script>
<!--  -->
<!--  <div class="text-center"></div>
            -->
