<template>
   <div>
      <h1>{{ name }}</h1>
      <button v-on:click="name='Aung Aung'">Change Name</button>
      <h4>{{ count }}</h4>
      <button @click="increase(1)">Increase 1</button>
      <button @click="increase(5)">Increase 5</button>
      <button @click="decrease(1)">Decrease 1</button>
      <button @click="decrease(5)">Decrease 5</button>
   </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      name:'nay zaw aung',
      count:0,
    }
  },
methods:{
   increase(num){
    this.count += num
   },
   decrease(num){
    this.count -= num
   }
},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
