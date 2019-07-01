<template>
  <div id="app">
    <Head></Head>
    <search></search>
    <navSlider></navSlider>
    <Exam></Exam>
    <Pec></Pec>
    <Taocan></Taocan>
    <SalTime></SalTime>
    <Mainitem></Mainitem>
      <BrandShow></BrandShow>
    <Promise></Promise>
    <Introduce></Introduce>
    <About></About>
  </div>
</template>

<script>
import Head from './components/Head'
import  Search from './components/Search'
import  navSlider from './components/navSlider'
import  Exam from  './components/Exam'
import  Pec from './components/Pec'
import Taocan from './components/Taocan'
import SalTime from './components/SalTime'
import  Mainitem from './components/Mainitem'
import  BrandShow from './components/BrandShow'
import Promise from './components/Promise'
import Introduce from './components/Introduce'
import About from './components/About'

export default {
  name: 'app',
  components: {
    Head,
    Search,
    navSlider,
    Exam,
    Pec,
    Taocan,
    SalTime,
    Mainitem,
    BrandShow,
    Promise,
    Introduce,
    About
  }
}
</script>

<style>
*{
  padding: 0px;
  margin: 0px;
  list-style: none;
  text-decoration: none;
}
@media only screen and (min-width: 1400px) and (max-width: 2000px){
  html{
  font-size: 62.5%;
}
}
@media only screen and (max-width: 1400px){
  html{
    font-size: 7px;
  }
}

body{
  min-width: 1200px;
}

  #app{
    min-width: 1200px;
    background-color: rgb(241,241,241);
    width: 100%;
  }
</style>
