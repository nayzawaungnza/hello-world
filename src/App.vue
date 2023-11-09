<template>
   <div>
    <pre>
      {{ JSON.stringify(formValues, null, 2) }}
    </pre>
    <form>
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
      }
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
