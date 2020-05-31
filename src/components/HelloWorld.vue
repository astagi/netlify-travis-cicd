<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      Learn how to setup <a href="https://github.com/astagi/netlify-travis-cicd" target="_blank" rel="noopener">CI/CD with TravisCI and Netlify</a>, configuring TravisCI to run tests, build site and then deploy on Netlify.
    </p>
    <hr>
    <p>
      For more about CI/CD with TravisCI and Netlify <a href="https://dev.to/astagi/continuous-integration-and-deployment-with-travisci-and-netlify-4294" target="_blank" rel="noopener">read this article</a>
    </p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

@Component
export default class HelloWorld extends Vue {
  @Prop() private msg!: string;
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
hr {
  border: 1px solid #41B883;
}
h3 {
  margin: 40px 0 0;
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
