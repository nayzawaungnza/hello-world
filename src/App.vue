<template>
   <div>
    <h1>Full Name - {{ firstName }} {{ lastName }}</h1>
    <h3>Computed Full name - {{ fullName }}</h3>
    <h2>Total - {{ items.reduce((total,current)=>(total = total + current.price),0) }}</h2>

    <h6>Computed Total - {{ total }}</h6>

    <button @click="items.push({id:4,title:'PC',price:400})">Add Item</button>
   </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      firstName:'Nay Zaw',
      lastName: 'Aung',
      items:[
          {
            id:1,
            title:'TV',
            price:100,
          },
          {
            id:2,
            title:'Phone',
            price:200,
          },
          {
            id:3,
            title:'Laptop',
            price:300,
          },
      ],
    }
  },
methods:{
  
},
computed:{
  fullName(){
    return `${this.firstName} ${this.lastName}`
  },
  total(){
    return this.items.reduce((total,current)=>(total = total + current.price),0)
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
