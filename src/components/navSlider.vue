<template>
<div class="nav-slider">
    <div class="nav">
        <ul>
            <li  v-for="(site,index) in navName" @click="tab(index)" :class="{active:index==id}"><a href="#">{{site}}</a></li>
        </ul>
    </div>
    <div class="slider">
        <div v-show="id===0" class="quick">
            <ul class="qCon">
                <li>快速预约体验套餐</li>
                <li><span>价位</span><input class="inp" type="text" placeholder="300~500元  500~1000元  1500元以上"></li>
                <li><span>性别</span><div class="check">
                    <div>男女通用<input type="radio" name="sex" value="common"></div>
                    <div>男性<input type="radio" name="sex" value="male"></div>
                    <div>女性<input type="radio" name="sex" value="female"></div>
                </div></li>
                <li><span>性质</span><select>
                    <option value="内科体检">内科体检</option>
                    <option value="全身体检">全身体检</option>
                    <option value="包治百病">包治百病</option>
                    <option value="药到病除">药到病除</option></select></li>
                <li><span>类型</span><input class="inp" type="text" placeholder="三甲医院 专业体检中心 公立医院"></li>
                <li><input class="btn" type="button" value="搜索"></li>
            </ul>
        </div>
            <!-- swiper -->
            <swiper :options="swiperOption">
                <swiper-slide v-for="imgsrc in imgSrc"><img :src="imgsrc" alt=""></swiper-slide>
                <div class="swiper-pagination" slot="pagination"></div>
                <div class="swiper-button-prev swiper-button" slot="button-prev"></div>
                <div class="swiper-button-next swiper-button" slot="button-next"></div>
            </swiper>
    </div>
</div>
</template>

<script>
    export default {
        name: "navSlider",
        data(){
            return{
                id:0,
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
        methods:{
            tab:function (index) {
                this.id = index;
            }
        }

    }
</script>

<style scoped>
.nav-slider{
    min-width: 1200px;
    width: 100%;
}
 .nav-slider .nav{
     width: 100%;
     background-color: rgb(52,181,242);
 }
 .nav-slider .slider{
     width: 100%;
     position: relative;

 }
 .nav-slider .slider .quick{
     position: absolute;
     width: 20%;
     height: 90%;
     padding: 1rem 1.5rem 0;
     background-color: #ffffff;
     border: 1rem solid rgba(200,200,200,0.2);
     top: 0px;
     left: 10rem;
     z-index: 999;
 }
  .slider .quick .qCon{
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
  }
  .quick .qCon li{
      width: 100%;
      height: 15%;
      /*border: 1px solid red;*/
      display: flex;
      align-items: center;

  }
  .quick .qCon li .check{
      width: 80%;
      height: 100%;
      display: flex;
      padding-left: 5%;
      box-sizing: border-box;
      justify-content: center;
  }
  .quick .qCon li .check div{
      width: 33%;
      height: 100%;
      display: flex;
      align-items: center;
  }
  .qCon li .check div input{
      width: 20%;
      height: 40%;
      margin-left: 10%;
      border: none;
  }
  .quick .qCon li span{
      position: relative;
      width: 20%;
      height: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
  }
  .quick .qCon li span:after{
      position: absolute;
      content: '';
      border-right: 0.2rem solid #22aaff;
      width: 100%;
      height: 70%;
  }
  .quick .qCon li:nth-of-type(1){
      justify-content: center;
      font-size: 1.8rem;
      font-weight: bold;
  }
  .quick .qCon li:nth-of-type(n+2){
      border: 1px solid #cccccc;
  }
  .quick .qCon li .inp,select{
      width: 80%;
      height: 100%;
      text-indent: 5%;
      border: none;
      font-size: 1.1rem;
  }
  .quick .qCon li .btn{
      width: 100%;
      height: 100%;
      border: none;
      background-color: #22aaff;
      color: #ffffff;
      font-size: 2rem;
      font-weight: bold;
      cursor: pointer;
  }
  .nav ul {
      width: 100%;
      box-sizing: border-box;
      height: 100%;
      padding: 0 100px;
      display: flex;
  }
.nav ul li{
    width: 10%;
    line-height: 6rem;
    text-align: center;
    }
.nav ul li.active{
    background-color:rgb(27,162,230);
}
.nav ul li a{
    font-size: 1.4rem;
    color: #eeeeee;
    font-weight: bold;
}
.slider img{
    width: 100%;
    height: 100%;
}


</style>
