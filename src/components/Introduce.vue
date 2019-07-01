<template>
<div class="introduce">
    <div class="introCon">
        <div class="introCity">
            <h3>福州介绍</h3>
            <p>福州体检预约中心为你提供福州体检预约、体检套餐预定服务、在此有大量福州体检中心/机构供你选择，您可以免费查询、比较体检项目和体检价格，为您的健康体检做准备。</p>
        </div>
        <div class="otherCity">
            <h3>福州体检城市</h3>
            <div class="cityName">
                <span>福清体检</span>
                <span>厦门体检</span>
                <span>莆田体检</span>
                <span>南平体检</span>
            </div>
        </div>
        <div class="hotCity">
            <div class="hotName">
                <span>全国体检热门城市</span>
                <span class="activeCity">城市入职体检</span>
                <span>热门体检中心</span>
            </div>
            <div class="hotList">
            <span v-for="city in hotCity">{{city}}</span>
            </div>
        </div>
        <div class="link">
            <h3>友情链接</h3>
            <div class="linkName">
                <a v-for="link in linkname" href="#">{{link}}</a>
            </div>
        </div>
    </div>
</div>
</template>

<script>
    export default {
        name: "Introduce",
        data(){
            return{
                hotCity:['北京入职体检','上海入职体检','长沙入职体检','郑州入职体检','成都入职体检','重庆入职体检','杭州入职体检',
                '广州入职体检','合肥入职体检','深圳入职体检','武汉入职体检','哈尔滨入职体检','南京入职体检','西安入职体检','青岛入职体检'],
                linkname:['体检项目','护发','症状库','回春医药','男科疾病','福州二手房','仲景健康网','台湾体检','日本体检','四海养生网',
                '口腔保健','临床医师资格','福州商铺网','福州黄页','疾病保健','母婴保健','福州天气','中商健康','胃肠','福州地图','广州体检']
            }
        }
    }
</script>

<style scoped>
.introduce{
    min-width: 1200px;
    width: 100%;
    padding: 3rem 10rem;
    box-sizing: border-box;
    font-size: 1.6rem;
}
 .introduce .introCon{
     width: 100%;
     /*border: 1px solid green;*/
     display: flex;
     flex-direction: column;
 }
    .introduce .introCon .introCity,.otherCity,.hotCity,.link{
        width: 100%;
        padding:1rem 0px;
        border-bottom: 1px dashed #b3b3b3;
        display: flex;
        flex-direction: column;
    }
    .introCity h3{
        font-size: 1.6rem;
        padding-bottom: 1rem;
    }

    .introCity p {
        padding: 0.5rem 0px;
        color: #666666;
        font-size: 1.4rem;
    }

    .otherCity h3{
        font-size: 1.6rem;
        padding-bottom: 1rem;
    }
    .otherCity .cityName {
        padding-top: 1rem;
    }
    .otherCity .cityName span{
        padding:0 1rem;
        font-size: 1.4rem;
        color: #666666;

    }
    .otherCity .cityName span:nth-of-type(1){
        padding-left: 0px;
    }
    .introCon .hotCity .hotName{
        padding-bottom: 2rem;
    }
    .introCon .hotCity .hotName span{
        font-size: 1.6rem;
        font-weight: bold;
        margin-right: 1rem;
        color: #666666;
        cursor: pointer;
    }
    .hotCity .hotName span.activeCity{
        color:#22aaff;
    }
    .introCon .hotCity .hotList{
        width: 90%;
        display: flex;
        flex-wrap: wrap;
    }
    .hotCity .hotList span{
        display: inline-block;
        padding-left: 1rem;
        padding-bottom: 1rem;
        font-size: 1.4rem;
        color: #666666;

    }
    .introCon .link{
        border-bottom: none;
    }
    .introCon .link h3{
      font-size: 1.6rem;
        padding-bottom: 1rem;
    }
    .introCon .link .linkName{
        width: 90%;
        display: flex;
        flex-wrap: wrap;
    }
    .link .linkName a{
        display: inline-block;
        padding: 1rem 1.5rem;
        font-size: 1.4rem;
        color: #666666;
    }


</style>
