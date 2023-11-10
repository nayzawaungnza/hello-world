<template>
   <div>
    <h1>Volume Tracker - [0-20]</h1>
    <h3>Current Volume - {{ volume }}</h3>
    <div>
      <button @click="volume += 2">Increase</button>
      <button @click="volume -= 2">Decrease</button>
    </div>
    <input type="text" v-model="movie" name="" id="">

    <div>
      <input type="text" v-model="movieInfo.title" name="" id="">

    <input type="text" v-model="movieInfo.actor" name="" id="">
    </div>
    <div>
      <button @click="movieList.push('Wonder Woman')">Add Movie</button>

      <button @click="movieList = movieList.concat(['Wonder Woman'])">Add Movie</button>
    </div>
   </div>

   
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      volume:0,
      movie:'Batman',
      movieInfo:{
        title:'',
        actor:'',
      },
      movieList:['Batman','Superman','Antman'],
    }
  },
methods:{},
computed:{},
watch:{
  volume(newVolume, oldVolume){
      if(newVolume> oldVolume && newVolume === 16){
        alert('Listening to a high volume for a long time may damage your hearing')
      }
  },
  movie:{
      handler(newMovie){
      console.log(`calling api - ${newMovie}`);
    },
    immediate:true,
  },
  movieInfo:{
    handler(newMovie){
      console.log(`Calling api = ${newMovie.title} and ${newMovie.actor}`);
    },
    deep:true,
  },
  movieList:{
    handler(newMovie){
      console.log(`Update movie list ${newMovie}`);
    },
    //deep:true, //push () using deep:true, concat() not using deep:true
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
