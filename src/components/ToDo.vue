<template>
  <div class="todos">
    <h1>Todo App</h1>
    <input @keyup.enter="add" type="text" v-model="title" placeholder="What you want to do?">
    <button @click="add">Add to list</button>
<ul><li v-for="(todo,index) in todos">{{todo}}
  <span @click="remove(index)" class="remove">x</span>
</li></ul>
</div>  
</template>



<script>
export default {
  name: "todo",
  props: {
    msg: String
  },
  data(){
    return{
      title:'',
      todos:['Go to shop']
    }
  },
  methods:{
    remove(id){
      //console.log(id);
    //  this.todos.splice(id,1);
      this.$delete(this.todos, id);

    },
    add(){
      if(this.title!=''){
       //this.todos.push(this.title),
        this.todos.unshift(this.title),
this.title=""}
           
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.remove{
  padding: .3rem .6rem;
  background-color: red;
  color: white;
  border-radius: 30px;
}
.remove:hover{cursor: pointer;}
ul li{padding: .4rem;}
</style>
