<template>
<div class="nav-slider">
    <div class="nav">
        <ul>
            <li  v-for="site in navName"><a href="#">{{site}}</a></li>
        </ul>
    </div>
    <div class="slider">
        <md-card>
        <md-card-media>
            <!-- swiper -->
            <swiper :options="swiperOption">
                <swiper-slide v-for="imgsrc in imgSrc"><img :src="imgsrc" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
                <div class="swiper-button-prev swiper-button" slot="button-prev"></div>
                <div class="swiper-button-next swiper-button" slot="button-next"></div>
            </swiper>
        </md-card-media>
        </md-card>

    </div>
</div>
</template>

<script>
    export default {
        name: "navSlider",
        data(){
            return{
                navName:['首页','体检机构','体检套餐','入职体检','Pet-ct检查','企业团检','我的服务','全球医疗','体检报告查询'],
                swiperOption: {
                    spaceBetween: 30,
                    centeredSlides: true,
                    autoplay: {
                        delay: 2500,
                        disableOnInteraction: false
                    },
                    pagination: {
                        el: '.swiper-pagination',
                        clickable: true
                    },
                    navigation: {
                        nextEl: '.swiper-button-next',
                        prevEl: '.swiper-button-prev'
                    }
                },
                imgSrc:[require('../assets/images2/7.jpg'),require('../assets/images2/7.jpg'),require('../assets/images2/7.jpg')]
            }
        },

    }
</script>

<style scoped>
.nav-slider{
    width: 100%;
    height: 470px;
}
 .nav-slider .nav{
     width: 100%;
     height: 65px;
     background-color: rgb(52,181,242);
 }
  .nav ul {
      width: 100%;
      box-sizing: border-box;
      height: 100%;
      padding: 0 100px;
  }
.nav ul li{
    float: left;
    height: 65px;
    padding: 0 40px;
    line-height: 65px;
    }
.nav ul li.active{
    background-color:rgb(27,162,230);
}
.nav ul li a{
    font-size: 18px;
    color: #eeeeee;
    font-weight: bold;
}
    .swiper-button{
        color: #ffffff;
    }

</style>
