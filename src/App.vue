<template>
   <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
    <form @submit="submitForm">
      <div class="rendered-form">
        <div class="formbuilder-text form-group field-name">
            <label for="name" class="formbuilder-text-label">Name</label>
            <input type="text" class="form-control" name="name" v-model="formValues.name">
        </div>
    </div>
    <div class="rendered-form">
        <div class="formbuilder-text form-group ">
            <label for="profile" class="formbuilder-text-label">Profile Summary</label>
            <textarea class="form-control" name="profile" v-model="formValues.profileSummeery"></textarea>
        </div>
    </div>

    <div class="rendered-form">
    <div class="formbuilder-select form-group field-country">
        <label for="country" class="formbuilder-select-label">Country</label>
        <select class="form-control" name="country" id="country" v-model="formValues.country">
          <option value="" >Select country</option>
            <option value="myanmar" >Myanmar</option>
            <option value="singapore" id="country-1">Singapore</option>
            <option value="thailand" id="country-2">Thailand</option>
        </select>
    </div>
</div>

<div class="rendered-form">
    <div class="formbuilder-select form-group field-country">
        <label for="joblocation" class="formbuilder-select-label">Job Location</label>
        <select class="form-control" name="joblocation" id="joblocation" multiple v-model="formValues.jobLocation">
            <option value="myanmar" >Myanmar</option>
            <option value="singapore" id="country-1">Singapore</option>
            <option value="thailand" id="country-2">Thailand</option>
        </select>
    </div>
</div>

<div class="rendered-form">
    <div class="formbuilder-checkbox-group form-group field-remote-work">
        <div class="checkbox-group">
            <div class="formbuilder-checkbox">
                <input name="remote-work[]" true-value="yes" false-value="no" v-model="formValues.remoteWork" id="remote-work-0" value="open-to-remote-work" type="checkbox" checked="checked">
                <label for="remote-work-0">Opent to remote work!</label>
            </div>
        </div>
    </div>
</div>
<div>
  <label for="html">HTML</label>
  <input type="checkbox"  value="html" id="html" v-model="formValues.skillSet">
  <label for="js">JS</label>
  <input type="checkbox"  value="js" id="js" v-model="formValues.skillSet">
  <label for="php">PHP</label>
  <input type="checkbox"  value="php" id="php" v-model="formValues.skillSet">
  <label for="vue">Vue</label>
  <input type="checkbox"  value="vue" id="vue" v-model="formValues.skillSet">
</div>

<div>
  <label >Experience</label>
  <input type="radio"  value="0-2" id="0-2" v-model="formValues.yearOfExperience">
  <label for="0-2">0 - 2</label>
  <input type="radio"  value="2-5" id="2-5" v-model="formValues.yearOfExperience">
  <label for="2-5">2 - 5</label>
  <input type="radio"  value="5-10" id="5-10" v-model="formValues.yearOfExperience">
  <label for="5-10">5 - 10</label>
  <input type="radio"  value="10+" id="10+" v-model="formValues.yearOfExperience">
  <label for="10+">10+</label>
</div>
<div>
  <button>Submit</button>
</div>

    </form>
   </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return{
      formValues:{
        name:'',
        profileSummeery:'',
        country:'',
        jobLocation:[],
        remoteWork:'no',
        skillSet:[],
        yearOfExperience:'',
      }
    }
  },
methods:{
  submitForm(event){
    event.preventDefault()
    console.log('Form Value ' , this.formValues)
    
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
