<template>
  <div id="app">
    <Header />
    <Banner :link="$url+'y3zct'" :header="['id','title','image_url']" />
    <Products :link="$url+'dbycd'" :header="['id','name','image_url']" />
    <b-container ><b-row align-content-center>
        <b-col sm="8"> <About /> </b-col>
        <b-col sm="4"> <News /> </b-col>
    </b-row></b-container>
    <Content />
    <Partners />
    <Contact />
    <Footer />
  </div>
</template>

<script>

//import Header from './components/Header'
//import Banner from './components/Banner'
//import Products from './components/Products'
//import About from './components/About'
//import News from './components/News'
//import Partners from './components/Partners'

import Vue from 'vue';

//import BootstrapVue from 'bootstrap-vue'
//Vue.use(BootstrapVue)

import { LayoutPlugin } from 'bootstrap-vue'
Vue.use(LayoutPlugin)
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

//Vue.config.silent = true

//Vue.prototype.$url = 'https://api.myjson.com/bins/'
Vue.prototype.$url = ''

export default {
  name: 'app',
  components: {
    //Header,
    //Banner,
    //Products,
    //About,
    //News,
    //Partners,
    //Contact,
    //Footer,
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Montserrat-Bold', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: .55rem;
}
</style>
