<template>
  <div id="app">
    <Header />
    <Banner :link="$url+'y3zct'" :header="['id','title','image_url']" />
    <Products :link="$url+'dbycd'" :header="['id','name','image_url']" />
    <b-container id="meio"><b-row>
        <b-col lg="8"> <About /> </b-col>
        <b-col lg="4"> <News :link="$url+'11qq59'" :header="['id','description','published_at']" /> </b-col>
    </b-row></b-container>
    <!--Partners :link="$url+'qfhnh'" :header="['id','name','image_url']" />
    <Contact />
    <Footer /-->
  </div>
</template>

<script>

import Header from './components/Header'
import Banner from './components/Banner'
import Products from './components/Products'
import About from './components/About'
import News from './components/News'
//import Partners from './components/Partners'
//import Partners from './components/Contact'
//import Partners from './components/Footer'

import Vue from 'vue';

import { LayoutPlugin } from 'bootstrap-vue'
Vue.use(LayoutPlugin)
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'

//Vue.config.silent = true

Vue.prototype.$url = 'https://api.myjson.com/bins/'

export default {
  name: 'app',
  components: {
    Header,
    Banner,
    Products,
    About,
    News,
    //Partners,
    //Contact,
    //Footer,
  }
}
</script>

<style scoped lang="scss">

@media (min-width:768px) { #meio{margin-top: 3.9rem;}}

.col-lg-8, .col-lg-4{
  padding:0;
}

</style>

<style lang="scss">
#app {
  font-family: 'Montserrat-Bold', 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: .55rem;
  outline: none;
}
</style>
