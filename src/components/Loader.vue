<script setup>
import gsap from 'gsap';
import { onMounted, ref } from 'vue';
const isLoading = ref(true);
const cube1 = ref(null);
const cube2 = ref(null);
const cube3 = ref(null);
const cube4 = ref(null);
const t1 = gsap.timeline({repeat:-1});


onMounted(()=>{
  t1.fromTo(cube1.value,{x:-50},{x:0,duration:0.3})
    .fromTo(cube2.value,{x:-10},{duration:0.1,x:10})
    .fromTo(cube3.value,{x:-10},{duration:0.1,x:10})
    .fromTo(cube4.value,{x:0},{duration:0.3,x:50})
    .fromTo(cube4.value,{x:50},{duration:0.3,x:0})
    .fromTo(cube3.value,{x:10},{duration:0.1,x:-10})
    .fromTo(cube2.value,{x:10},{duration:0.1,x:-10})
    .fromTo(cube1.value,{x:10},{x:-50,duration:0.3})
});

</script> 
<template>
  <div class="pageloader">
    <div class="cube" ref="cube1"></div>
    <div class="cube" ref="cube2"></div>
    <div class="cube" ref="cube3"></div>
    <div class="cube" ref="cube4"></div>
  </div>


</template>
<style  scoped>
.pageloader {
  display: flex;
  width:100%
}

.cube {
  width: 30px;
  height: 30px;
  margin: 3px;
}

.cube:nth-child(1) {
  background-color: blue;
  border-radius: 50%;
}

.cube:nth-child(2) {
  background-color: brown;
  border-radius: 50%;
}

.cube:nth-child(3) {
  background-color: green;
  border-radius: 50%;
}

.cube:nth-child(4) {
  background-color: black;
  border-radius: 50%;
}</style>

