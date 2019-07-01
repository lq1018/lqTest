<template>
<div class="Sale">
    <div class="title"><a href="#"><span>限时</span>特惠区</a></div>
    <ul>
        <li v-for="imgSrc in saleData"><a href="#"><img :src="imgSrc" alt=""></a></li>
    </ul>
</div>
</template>

<script>
    export default {
        name: "SalTime",
        data(){
            return{
                saleData:[require('../assets/images2/4.gif'),require('../assets/images2/4.gif'),require('../assets/images2/4.gif'),require('../assets/images2/4.gif')]
            }
        }
    }
</script>

<style scoped>
.Sale{
    min-width: 1200px;
    box-sizing: border-box;
    width: 100%;
    padding: 0 10rem;
}
 .Sale .title{
     box-sizing: border-box;
     width: 100%;
     margin-top: 3rem;
     background-color: #ffffff;
     line-height: 6rem;
     padding-left: 2rem;
 }
 .Sale .title a{
     font-size: 2.4rem;
     color: #3a3a3a;
 }
  .Sale .title a span{
      color: #22aaff;
  }
   .Sale ul{
       width: 100%;
       margin-top: 3rem;
       display: flex;
       justify-content: space-between;
   }
    .Sale ul li{
        box-sizing: border-box;
        width: 24%;
        background-color: #ffffff;
        padding: 1.5rem 1rem 3rem;
    }
    .Sale ul li a img{
        width: 100%;
    }
</style>
