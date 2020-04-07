<template lang="pug">
  div(class="about")
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';

@Component({
  name: 'About',
  components: {
  },
})
export default class App extends Vue {}
</script>

<style lang="scss">
  .about{
    background: pink;
    height: 100vh;
  }
</style>
