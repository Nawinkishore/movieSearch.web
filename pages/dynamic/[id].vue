<template>
    <div>
        <div>
          <p>Student id:{{studentId}}</p>  
        </div>
    </div>
</template>
<script>
export default{
    data(){
        return{
            studentId:this.$route.params.id,
        }
    }
}
</script>