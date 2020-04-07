<template lang="pug">
  div(class="work-three")
    video(width="700" height="500" poster="../images/gaia.gif" id="video" preload v-on:mouseover="handleMouseOver")
      source(src="../images/gaia.gif" type="video/mp4" )
    p(class="about-gaia")
      | Gaia Protection is a non-profit located in Bamburg, Germany. I am working with Gaia to build an intereactive map for locating and connecting sustainably inspired volunteer opportunities all acreoss the world.
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'WorkThree',
  components: {
  },
})
export default class App extends Vue {}
</script>

<style lang="scss" scoped>
  .work-three{
    background: #FFFEF4;
    height: 100vh;
  }

  #video{
    position: relative;
    left: 4vw;
    top: 10vh;
  }

  .about-gaia{
    width: 30vw;
    position: relative;
    bottom: 60vh;
    left: 68vw;
    color: black;
    font-size: 30px;
  }
</style>
