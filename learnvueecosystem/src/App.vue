<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">


  <div class="progress">
    <div id='bar'></div>
  </div>

<button @click="animateProgressBar">animate progress bar</button>
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>

</template>

<script>
import $ from 'jquery'
export default {
  name: 'app',
  methods:{
    animateProgressBar(){
      $('#bar').removeClass('transition');
            $('#bar').css({
        'width':'0%',
        'background-color':'transparent'
      });

setTimeout(()=>{
      $('#bar').addClass('transition');
      $('#bar').css({
        'width':'100%',
        'background-color':'black'
      });
},100);


    }
  }
}
</script>

<style  scoped>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}


.progress {
  height: 16px;
  background-color: silver;
}

#bar{
  height: 16px;
}

.transition{
    transition: 0.4s linear;
  transition-property: width, background-color;
}
</style>

