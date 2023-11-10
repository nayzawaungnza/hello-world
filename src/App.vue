<template>
   <div>
    <h1 v-once>{{ name }}</h1>
    <button @click="name='Thinzar'">Change Name</button>
    <h3 v-pre>{{ name }}</h3>
   </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      name:'nay zaw aung',
    }
  },
methods:{
  
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
