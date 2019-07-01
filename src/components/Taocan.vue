<template>
<div class="taocan">
     <div class="tc-nav">
        <ul>
            <li><span>精选</span>体验套餐</li>
        </ul>
        <ul>
            <li v-for="(exam,index) in examData" @click="tab(index)"><a href="" :class="{active : currentIndex==index}">{{exam}}</a></li>
            <li><a href="#">更多</a></li>
        </ul>
    </div>
      <div class="tc-content">
        <ul v-for="site in contentData">
           <li><img :src="site.imgSrc" alt=""></li>
           <li>
               <div class="wrap">
                  <h3>{{site.hostName}}</h3>
                  <div class="detail">
                      <p>适宜人群：{{site.people}}</p>
                      <p>所属医院：{{site.hostDress}}</p>
                      <p>体检时间：{{site.time}}</p>
                  </div>
                  <div class="bottom">
                      <div>已售：{{site.saleNum}} 评价 {{site.commentNum}}</div>
                      <div><span>￥{{site.originPrice}}</span>￥{{site.currentPrice}}</div>
                  </div>
               </div>
               </li>
        </ul>
    </div>
</div>
</template>

<script>
    export default {
        name: "Taocan",
        data(){
            return{
                examData:['职场白领','入职体检','老年体检','孕前体检','常规体检','全身体检','中老年体检'],
                contentData:[{
                    imgSrc:require('../assets/images2/3.jpg'),
                    hostName:'福州市中医院健康体检中心男性心理体检非积分不给分解符捏',
                    people:'中年男性，老年男性',
                    hostDress:'福建中医药大学附属福州中医院体检中心',
                    time:'周一-周五7:30-12:00(10:00前抽血截至)',
                    saleNum:396,
                    commentNum:71,
                    originPrice:1820,
                    currentPrice:1646.8
                },
                {
                    imgSrc:require('../assets/images2/3.jpg'),
                    hostName:'福州市第一医院健康体检中心男性',
                    people:'中年男性，青年男性，老年男性',
                    hostDress:'福州市第一医院体检中心',
                    time:'周一-周日7:30-12:00(抽血时间为10:30之前)',
                    saleNum:744,
                    commentNum:271,
                    originPrice:700,
                    currentPrice:640
                },
                {
                    imgSrc:require('../assets/images2/3.jpg'),
                    hostName:'福州市地质医院关爱青年体检套餐',
                    people:'青年男性，亚健康人群',
                    hostDress:'福州市地质医院体检中心',
                    time:'周一-周日，上午：7:30-12:00 下午：14:00-17:00',
                    saleNum:566,
                    commentNum:181,
                    originPrice:500,
                    currentPrice:400
                },
                {
                    imgSrc:require('../assets/images2/3.jpg'),
                    hostName:'福建医科大学附属第一医院体检套餐',
                    people:'已婚女性，青年女性，中年女性',
                    hostDress:'福建医科大学附属第一医院体检中心',
                    time:'周一-周六7:30-12:00',
                    saleNum:124,
                    commentNum:71,
                    originPrice:1030,
                    currentPrice:950
                }
                ],
                currentIndex:0
            }
        },
        methods:{
            tab:function(index){
              this.currentIndex = index;
            }
        }
    }
</script>

<style scoped>
.taocan{
    min-width: 1200px;
    width: 100%;
    padding: 0 10rem;
    box-sizing: border-box;
}
    .taocan .tc-nav{
        width: 100%;
        margin-top: 3rem;
        background-color: #ffffff;
        display: flex;
    }
    .taocan .tc-nav ul:nth-child(1){
        flex-grow: 2;
    }
    .tc-nav ul:nth-child(1) li{
        box-sizing: border-box;
        width: 100%;
        line-height: 6rem;
        padding-left: 2rem;
        font-size: 2.4rem;
        color: #3a3a3a;
    }
    .tc-nav ul:nth-child(1) li span{
               color: #22aaff;
    }
    .taocan .tc-nav ul:nth-child(2){
        flex-grow: 8;
        display: flex;
        justify-content: flex-end;
    }
    .tc-nav ul:nth-child(2) li{
        display: flex;
        width: 10%;
        align-items: center;
        margin:0 0.5rem;
    }
    .tc-nav ul:nth-child(2) li:last-of-type{
        border-left: 1px solid #dddddd;
    }
    ul:nth-child(2) li a{
        width: 100%;
        padding: 0.5rem 0.6rem;
        text-align: center;
        border-radius: 0.5rem;
        color:#666666;
        font-size: 1.4rem;
        font-weight: bold;
    }
    ul:nth-child(2) li a.active{
          background-color: #22aaff;
        color: #ffffff;
        border-radius: 0.5rem;
    }
    .taocan .tc-content{
        width: 100%;
        margin-top: 3rem;
        display: flex;
        justify-content: space-between;
    }
    .tc-content ul{
        width: 23%;
        border: 1px solid green;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        background-color: #ffffff;
    }
    .tc-content ul li:nth-of-type(1){
        width: 100%;
        /*border-bottom: 1px solid red;*/
    }
    .tc-content ul li:nth-of-type(2){
        width: 100%;
        padding: 1rem;
        box-sizing: border-box;
    }
    .tc-content ul li:nth-of-type(2) .wrap{
        width: 100%;
        display: flex;
        flex-direction: column;
    }
    .wrap h3{
        width: 100%;
        font-size: 1.6rem;
        font-weight: bold;
        color: #3a3a3a;
        padding: 1rem 0;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
    .wrap .detail{
        width: 100%;
        height: 12rem;
    }
    .wrap .detail p{
        padding: 0.5rem 0;
      font-size: 1.2rem;
      color: #666666;
    }
    .wrap .bottom{
        width: 100%;
        display: flex;
        justify-content:space-between;
        align-items: center;
    }
    .wrap .bottom div:nth-of-type(1){
        font-size: 1.2rem;
        color: #666666;
    }
    .wrap .bottom div:nth-of-type(2){
        color: orange;
        font-size: 1.6rem;
        font-weight: bold;
    }
    .wrap .bottom div:nth-of-type(2) span{
        font-size: 1.2rem;
        color: #aaaaaa;
        text-decoration: line-through;
    }
    .tc-content ul li:nth-of-type(1) img{
        width: 100%;
    }

</style>
