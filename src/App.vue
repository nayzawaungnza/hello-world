<template>
   
      <div>
        <h2 v-for="(name, index) in names" :key="name" > {{ index }} {{ name }}</h2>
        <h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>
        <div v-for="actor in actors" :key="actor.name">
            <h2>{{ actor.name }}</h2>
            <p v-for="movie in actor.movies" :key="movie">{{ movie }} </p>
        </div>
        <h6 v-for="value in myInfo" :key="value">{{ value }}</h6>
        <h6 v-for="(value, key, index) in myInfo" :key="value">{{ index }} {{ key }} {{ value }}</h6>
      </div>
      <template v-for="name in names" :key="name">
        <h2>{{ name }}</h2>
        <input placeholder="Last name" />
        <hr>
      </template>
      <button @click="shuffle">shuffle!</button>

      <template v-for="name in names" :key="name">
        <h3 v-if="name === 'Aung Aung'">{{ name }}</h3>
      </template>
      
</template>

<script>
import _ from 'lodash';
export default {
  name: 'App',
  data(){
    return{
      names:['Nay zaw','Aung Aung','Maung Maung'],
      fullNames:[
        {first:'Nay', last:'Zaw'},
        {first:'Zaw', last:'Gyi'},
        {first:'Aung', last:'Min'},
        {first:'Loon', last:'Naw'},
        {first:'May', last:'Mie'},
    ],
    actors:[
      {
        name:'Nay Toe',
        movies:['Mone Swal','Kyauk Kyauk Kyauk']
      },
      {
        name:'Zan Kyi',
        movies:['Now & Ever','Mudras Calling']
      },
      {
        name:'Pyi Ti Oo',
        movies:['Red Cotton Silk Flower','Toe Kyaw Man Nae Nan San Tae Ywar']
      }
    ],
    myInfo:{//object
        name:'Nay Zaw',
        channel:'Developer NAY',
        course:'Vue JS',
    }
  }
},
methods:{
  shuffle(){
    console.log(this.names);
    this.names = _.shuffle(this.names);
  },
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
