<template>
  <div>
    
    <div
       
        class="grid items-center justify-center mt-5 text-white"
      >
        <img :src="items.img" alt="" />
        <p class="text-center">{{ items.Title }}</p>
        
      </div>
  </div>
</template>
<script>
export default {
  props: {
    items: {
      type: Object,
      default: Object,
    },
  },
};
</script>
