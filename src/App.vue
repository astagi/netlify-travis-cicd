<template>
  <div id="app">
    <img alt="Vue logo" src="https://travis-ci.org/images/logos/TravisCI-Mascot-1.png">
    <img alt="Vue logo" src="https://www.netlify.com/img/press/logos/logomark-light.png">
    <HelloWorld msg="CI/CD with TravisCI and Netlify"/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from './components/HelloWorld.vue';

@Component({
  components: {
    HelloWorld,
  },
})
export default class App extends Vue {}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
img {
  width: auto;
  height: 200px;
  padding: 1rem;
}
@media only screen and (max-width: 768px) {
  img {
    height: 100px;
  }
}
</style>
