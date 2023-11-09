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

    <h1 v-bind:style="{
      color:highlightColor,
      // 'font-size': headingSize + 'px',
      fontSize: headingSize + 'px',
      padding:'20px',
    }">Inline Style</h1>
    <h1 v-bind:style="headerStyleObject">Object style</h1>

    <div v-bind:style="[baseStyleObject, successStyleObject]">Success Style</div>
    <div v-bind:style="[baseStyleObject, dangerStyleObject]">Danger Style</div>

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
      highlightColor:'orange',
      headingSize:50,
      headerStyleObject:{
        color:'orange',
        fontSize:'40px',
        padding:'10px',
      },
      baseStyleObject:{
        fontSize:'50px',
        padding:'10px',
      },
      successStyleObject:{
        color:'green',
        border:'1px solid #090900',
        backgroundColor:'lightgreen',
        padding:'20px',
      },
      dangerStyleObject:{
        color:'white',
        border:'1px solid #090900',
        backgroundColor:'red',
        padding:'20px',
      }
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
