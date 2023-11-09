<template>
   <div>
    <h2>Add method - {{ add(10,2,34) }}</h2>
    <h2>Multiply method - {{ multiply(5) }}</h2>
    <h2>Multiply method - {{ multiply(baseValue) }}</h2>
   </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      basemultipleNumber:5,
      baseValue:6,
    }
  },
methods:{
    add(a,b,c){
      return a+b+c
    },
    multiply(num){
      return num*this.basemultipleNumber
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
