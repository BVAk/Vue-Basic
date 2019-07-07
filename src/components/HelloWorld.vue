<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <alert mode="primary">First alert</alert>
    <alert mode="danger">Second alert</alert>
    <alert mode="success">Last alert</alert>
    <div><input type="text" v-model="lastName" placeholder="Enter your name">
    <p>Welcome, {{lastName}}</p>
    </div>
    <button v-on:click="ClickMode">Click me</button>
    <input type="text" @keyup.enter="doSmth" placeholder="Please, write your code"></input>
    
    <h3></h3>
    <ul>
    <li v-for="person in students"> {{person}}   </li>
    </ul>
    </div>
</template>



<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String
  },
  data(){
    return{
      lastName:"",
      students:['Vika','Andrew','Artem']
    }
  },
  methods:{
    ClickMode:function(){console.log("You click on the button")
  },
  doSmth:function(){
    console.log('lala')
  }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
