<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header/>
    <main>
      <div class="content"></div>
      <Panel/>
    </main>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Panel from './components/Panel.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Header,
    Panel,
    Footer
  }
}
</script>

<style lang="scss">
@import './style/commons.scss';

.content{
  background: black;
  height: 100px;
}
</style>
