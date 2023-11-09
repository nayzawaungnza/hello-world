<template>
   <div>
      <h1>{{ name }}</h1>
      <button v-on:click="name='Aung Aung'">Change Name</button>
      <h4>{{ count }}</h4>
      <button @click="count +=1">Increase</button>
      <button @click="count -=1">Decrease</button>
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
   increase(){
    this.count +=1
   },
   decrease(){
    this.count -= 1
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
