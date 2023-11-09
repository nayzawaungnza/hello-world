<template>
   <div>
      <h1>{{ name }}</h1>
      <button v-on:click="changeName($event), increase(1, $event)">Change Name</button>
      <h4>{{ count }}</h4>
      <button @click="increase(1, $event)">Increase 1</button>
      <button @click="increase(5, $event)">Increase 5</button>
      <button @click="decrease(1, $event)">Decrease 1</button>
      <button @click="decrease(5, $event)">Decrease 5</button>
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
  changeName(event){
      this.name = 'Aung Aung'
      console.log('Event' , event)
  },
   increase(num, event){
    this.count += num
    console.log('Event' , event)
   },
   decrease(num, event){
    this.count -= num
    console.log('Event' , event)
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
