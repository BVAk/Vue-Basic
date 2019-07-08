<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
   <HelloWorld msg="Welcome, my lovely Andrew"/>
  <todo></todo>
   <button-counter></button-counter>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "home",
  components: {
    HelloWorld
  }
};
</script>
