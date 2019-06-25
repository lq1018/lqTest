<template>
  <div id="app">
    <Head></Head>
    <search></search>
    <navSlider></navSlider>
    <Exam></Exam>
  </div>
</template>

<script>
import Head from './components/Head.vue'
import  Search from './components/Search'
import  navSlider from './components/navSlider.vue'
import  Exam from  './components/Exam.vue'

export default {
  name: 'app',
  components: {
    Head,
    Search,
    navSlider,
    Exam
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
  #app{
    background-color: rgb(241,241,241);
    width: 100%;
  }
</style>
