<template lang="pug">
  div(class="work-one")
    video(width="700" height="500" poster="../images/wf.gif" id="video" preload v-on:mouseover="handleMouseOver")
      source(src="../images/wf.gif" type="video/mp4" )
    p(class="about-wf")
      | West&Faring is a creative agency aimed at reimagining the way in which companies brand themselves. For this project, I used Vue.js with typescript and hosted it on a heroku web server
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'WorkOne',
  components: {
  },
})
export default class App extends Vue {

  private handleMouseOver() {
    var element = document.getElementById("video")
    if (element !== null) {
      // element.play();
    }
  }
}
</script>

<style lang="scss" scoped>
  .work-one{
    background: blue;
    height: 100vh;
  }

  #video{
    position: relative;
    left: 4vw;
    top: 10vh;
  }

  .about-wf{
    width: 30vw;
    position: relative;
    bottom: 60vh;
    left: 68vw;
    color: white;
    font-size: 30px;
  }
</style>
