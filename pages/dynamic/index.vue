<template>
  <div>
    <div>
      <h1>Hello</h1>
      <p v-for="(student,index) in students" :key="index"><NuxtLink :to="`/dynamic/${student.studentId}`">{{student.studentName}}</NuxtLink></p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      students: [
        {
          studentId: 1,
          studentName: "Nawin",
        },
        {
          studentId: 2,
          studentName: "Na",
        },
        {
          studentId: 3,
          studentName: "N",
        },
      ],
    };
  },
};
</script>
