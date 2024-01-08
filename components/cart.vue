<template>
  <div>
    
    <div
       
        class="grid items-center justify-center mt-5 text-white"
      >
        <img :src="item.img" alt="" />
        <p class="text-center">{{ item.Title }}</p>
      </div>
  </div>
</template>
<script>
export default {
  props: {
    item: {
      type: Object,
      default: Object,
    },
  },
};
</script>
