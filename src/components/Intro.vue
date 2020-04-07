<template lang="pug">
  div(class="intro")
    div(class="grid-container")
      h1(class="hello font" :style="{opacity: this.hello}")
        | HELLO.
      h1(class="i-am font" :style="{opacity: this.iAm}")
        | I AM
      h1(class="zach font" :style="{opacity: this.zach}")
        | ZACH
    img(src="../images/arrow.png" class="arrow")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'Intro',
  components: {
  },
})
export default class App extends Vue {
  public hello: number = 0;
  public iAm: number = 0;
  public zach: number = 0;

  public mounted() {
    this.hello = 1;
    this.iAm = 1;
    this.zach = 1;
  }
}
</script>

<style lang="scss">
  .intro{
    background: black;
    height: 100vh;
  }

  .grid-container{
    position: absolute;
    top: 8vh;
    left: 2vw;
    width: 96vw;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-areas: 
      "top"
      "middle"
      "bottom";
  }

  .font{
    color: white;
    font-size: 260px;
    line-height: 150px;
    font-family: 'Teko', sans-serif;
    margin: 0;
    align-self: start;
  }

  .hello{
    grid-area: top;
    justify-self: end;
    transition: all 2s;
  }

  .i-am{
    grid-area: middle;
    transition: all 0.7s;
  }

  .zach{
    grid-area: bottom;
    justify-self: end;
    transition: all 0.7s;
  }

  .arrow{
    width: 10vw;
    height: auto;
    position: absolute;
    top: 80vh;
    left: 45vw;
  }


</style>
