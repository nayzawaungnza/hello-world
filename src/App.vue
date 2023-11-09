<template>
   <div>
      <h2 v-if="num === 0">The Number is zero</h2>
      <h2 v-else-if="num < 0">The Number is negative</h2>
      <h2 v-else-if="num > 0">The Number is positive</h2>
    <h2 v-else>The Number is not a number</h2>
    <div v-if="display">
      <h3>De</h3>
      <h4>Develop</h4>
    </div>
   </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      num: 'Hi',
      display: true,
  }
}
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
