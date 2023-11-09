<template>
  <div>
     <h1>{{ greet }} {{ name }}</h1> <!-- Text Binding -->
     <p v-html="channel" ></p><!-- Binding HTML -->
     <div v-html="hack"></div>
     <h3 v-bind:id="headingID">Heading</h3> <!-- Attribute Binding -->
     <button v-bind:disabled="isDisabled">Bind</button>
     <h4 class="underline" v-bind:class="status">Underline</h4>
     <h4 v-bind:class="isPromoted && 'promoted'">Promoted Movies</h4>
     <h5 v-bind:class="isSoldOut ? 'sold-out':'new'">isSoldOut? movies</h5>
     <h5 v-bind:class="['new', 'promoted']">Newly Promoted Movies</h5>
     <h5 v-bind:class="[isPromoted&& 'promoted', isSoldOut?'sold-out':'new']">Array conditional movies</h5>
    <h5 v-bind:class="{
      promoted: isPromoted,
      new: !isSoldOut,
      'sold-out': isSoldOut,
    }">Object conditional movies</h5>

  </div>
</template>

<script>

export default {
  name: 'App',
  data(){
    return{
      greet:'Hello',
      name:'Nay Zaw',
      channel: '<b>Developer Nay</b>',
      hack: `<a href="#" onclick="alert('hacks')"> Win a Prize</a>`,
      headingID : 'heading',
      isDisabled: true,
      status:'success',
      isPromoted:true,
      isSoldOut:true,
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
.promoted{
  font-style: italic;
}
.success{
  color: green;
}
.underline{
  text-decoration: underline;
}
.new{
  color:olivedrab
}
.sold-out{
  color : red;
}
</style>
