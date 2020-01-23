<template>
  <div id = "app">
    <form action="">
    <h1>Sign up</h1>

    <div class="container">
      <label for="name">Username</label>
      <input 
              type="text"
              id = "name"
              placeholder="Enter Username"
              :value = "userData.name"
              @input = "userData.name = $event.target.value">
    </div>

    <div class = "container">
      <label for="email">Email</label>
      <input 
              type="text"
              id = "email"
              placeholder ="Enter Email"
              :value = "userData.email"
              @input = "userData.email = $event.target.value">
    </div>
    <div class = "container">
      <label for="password">Password</label>
      <input 
              type="password"
              id = "password"
              placeholder="Enter password"
              v.model.lazy = "userData.password">
              <p>{{userData.password}}</p>
    </div>
    <div class = "Checkbox">
      <label for="checkbox">
        <input 
              class = "input2"
              type="checkbox"
              id = "checkbox"
              v-model = "checked">Remember me</label>
        <span>Forgot <a :href= "link">password?</a> </span>
    </div>
    </form>
   
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      userData:{
        name: '',
        email:'',
        password:''
      },
      link:"#"
    }
  }
}
</script>

<style>
#app{
  font-family:Arial,Helvetica,sans-serif;
  margin-top:50px;
  font-size:16px;
  line-height:1.3em;
  align-items:center;
}
.container{
  text-align:center;
  padding:10px;
  margin-top:40px;

}
form{
  border:1px solid #DA7338;
  margin:2% 25%;
  height:auto;
  text-align:center;
  border-radius:20px;
}
h1{
  font-size:200%;
  margin-top:-30px;
}
input{
  background-color:#F0EEEE;
  border:1px solid #CBCBCB;
  border-radius:10px;
  padding:7px;
  width:60%;
  font-size:14px;
}
.input2{
  width:10px;
}
label{
  font-weight:bold;
  display:block;
  width:15%;
  float:left;
  text-align:left;
  margin-left:2%;
  padding-right:10px;
  min-width:120px;
}
.Checkbox{
margin-left:10%;
margin-right:10%;
font-size:0.8em;
align-items:center;
}
</style>