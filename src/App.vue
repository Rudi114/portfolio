<template lang="pug">
  div(class="app")
    Intro(class="scroll-item")
    WorkOne(class="scroll-item")
    WorkTwo(class="scroll-item")
    WorkThree(class="scroll-item")
    WorkFour(class="scroll-item")
    About(class="scroll-item")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

import Intro from '@/components/Intro.vue';
import WorkOne from '@/components/WorkOne.vue';
import WorkTwo from '@/components/WorkTwo.vue';
import WorkThree from '@/components/WorkThree.vue';
import WorkFour from '@/components/WorkFour.vue';
import About from '@/components/About.vue';



@Component({
  name: 'App',
  components: {
    Intro,
    WorkOne,
    WorkTwo,
    WorkThree,
    WorkFour,
    About
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">

  body{
    margin: 0;
  }

  .app {
    overflow-y: scroll;
    -webkit-overflow-scrolling: touch;
    scroll-snap-type: y mandatory;
    position: absolute;
    top: 0px;
    bottom: 0px;
    left: 0px;
    right: 0px;
  }
  .scroll-item {
    scroll-snap-align: start;
    scroll-snap-stop: always;
  }
</style>
