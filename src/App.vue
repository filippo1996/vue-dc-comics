<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header/>
    <Jumbotron/>
    <main>
      <GridProduct nameCategory="Current Series" :products="productsDc"/>
      <GridProduct nameCategory="BestSeller" :products="bestSeller"/>
      <Panel/>
    </main>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Jumbotron from './components/Jumbotron.vue';
import GridProduct from './components/GridProduct.vue'
import Panel from './components/Panel.vue';
import Footer from './components/Footer.vue';

//Items product DC
import DcComics from '@/data/DcComics.js';
import BestSeller from '@/data/BestSellerDc.js';

export default {
  name: 'App',
  components: {
    Header,
    Jumbotron,
    GridProduct,
    Panel,
    Footer
  },
  data(){
    return {
      productsDc: DcComics,
      bestSeller: BestSeller
    }
  }
}
</script>

<style lang="scss">
@import './style/commons.scss';

</style>
