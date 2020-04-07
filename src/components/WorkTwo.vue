<template lang="pug">
  div(class="work-two")
    video(width="700" height="500" poster="../images/vogon.gif" id="video" preload v-on:mouseover="handleMouseOver")
      source(src="../images/vogon.gif" type="video/mp4" )
    p(class="about-vogon")
      | VogonWeb is a product of GBCI at Arizona State Univerity. While working there, I used a Django Stack with Vue.js and Typscript for the front end. 
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'WorkTwo',
  components: {
  },
})
export default class App extends Vue {}
</script>

<style lang="scss" scoped>
  .work-two{
    background: green;
    height: 100vh;
  }

  #video{
    position: relative;
    left: 35vw;
    top: 10vh;
  }

  .about-vogon{
    width: 30vw;
    position: relative;
    bottom: 60vh;
    left: 2vw;
    color: white;
    font-size: 30px;
  }
</style>
