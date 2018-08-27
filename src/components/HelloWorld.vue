<template>
  <div class="hello">
   
    <mt-button size="large"  type="primary">66666</mt-button>
  </div>
</template>

<script>
import Vue from 'vue';
import MtButton from './button.vue'
//Vue.component(Button.name, Button);
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  components:{
    MtButton,
  }
  
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
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
