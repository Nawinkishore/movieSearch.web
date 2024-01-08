<template>
  <div>
    <div class="grid md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4">
        <div
      v-for="(list, index) in item"
      class="grid items-center justify-center mt-5 text-white "
    >
      <img :src="list.img" alt="" />
      <p class="text-center">{{ list.Title }}</p>
    </div>
    </div>
  </div>
</template>
<script>
export default{
    props:{
        item:{
            type:Array,
            default:Array,
        }
    },
}
</script>