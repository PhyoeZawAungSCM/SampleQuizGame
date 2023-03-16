<!-- <template>
  <div class="circle" ref="circle">
  </div>
  <div class="progress">
    <div class="progress-background"></div>
    <div class="progress-status" ref="progress"></div>
  </div>
  <button @click="move()">move</button>
  <input type="number" v-model="percentage"/>
  <div>
  <button @click="append">Append</button>
  <button @click="remove">Remove</button>
    <ul>
      <TransitionGroup appear name="list">
        <li v-for="i in data" :key="i">{{ i }}</li>
      </TransitionGroup>
    </ul>
  </div>
</template>
<script setup> 
  import {gsap} from 'gsap';
  import {ref,onMounted, computed,watch} from 'vue';
  const data = ref([1,2,3,4,5,6,7]);
  const circle = ref(null);
  const progress = ref(null);
  const percentage = ref(10);
  function remove(){
    data.value.shift()
  }
  function append(){
    data.value.push(data.value.length + 1);
  }
  watch(percentage,(p)=>{
    gsap.to(progress.value,{
      duration:1,
      width:p,
    })
    console.log(p)
  })
  console.log(circle);
  // onMounted(()=>{
  //   gsap.to(circle.value, {
  //   duration: 1.5,
  //   x: 100,
  // });
 // })
</script>
<style scoped >
.list-enter-active,
.list-leave-active {
  transition: all 0.5s ease;
}
.list-enter-from,
.list-leave-to {
  opacity: 0;
  transform: translateX(30px);
}
  .circle{
    background-color: rebeccapurple;
    width:40px;
    height: 40px;
    border-radius: 50%;
  }
  .progress{
    width:500px;
  }
  .progress-background{
    background-color: grey;
    width:100%;
    height: 5px;
  }
  .progress-status{
    background-color: pink;
    height: 5px;
    width:30px;
  }
</style> -->
<script setup>
 import Loader from './components/Loader.vue'
</script>
<template>
  <Loader/>
</template>
<style>
</style>