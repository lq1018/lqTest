<template>
<div class="Main">
    <ul class="wrapper">
        <li class="content" v-for="main in mainData">
            <div class="top">
                <div class="logo"><img :src="main.img1" alt=""></div>
                <div class="title">
                    <div>{{main.title1}}</div>
                    <div>{{main.title2}}</div>
                </div>
                <div class="more">更多</div>
            </div>
            <div class="center"><img :src="main.img2" alt=""></div>
            <ul class="bottom" >
                    <li class="news" v-for="news in main.News"><a href="#">{{news}}</a></li>
            </ul>
        </li>
        <li class="content">
            <div class="top">
                <div class="logo"><img src="../assets/images2/xinx.png" alt=""></div>
                <div class="title">
                    <div>体检项目知识</div>
                    <div>知识库</div>
                </div>
                <div class="more">更多</div>
            </div>
            <div class="center"><img src="../assets/images2/3.jpg" alt=""></div>
            <div class="tab">
                <div class="opt">
                    <span v-for="(item,index) in optName" @click="addClass(index)" :class="{active:index==optId}">{{item}}</span>
                </div>
                <div class="optContent">
                    <ul v-show="optId===0">
                        <li v-for="list in listName">{{list}}</li>
                    </ul>
                    <ul v-show="optId===1">box2</ul>
                    <ul v-show="optId===2">box3</ul>
                    <ul v-show="optId===3">box4</ul>
                </div>
            </div>
        </li>
    </ul>
</div>
</template>

<script>
    export default {
        name: "Mainitem",
        data(){
            return{
                mainData:[{
                    img1:require('../assets/images2/8.jpg'),
                    title1:'体检指南',
                    title2:'体检宝典',
                    img2:require('../assets/images2/9.jpg'),
                    News:['· 中国人减寿因素，每一个都离你很近','· 这样揉耳朵，等于给全身做一套“养生操”',
                    '· 魏总是不舒服，需要做胃镜吗？','· 小年遇到大汉，非得这样说吗？',
                    '· 我今天就要给各位OG打个样，呼吸不止，说唱不停，我们是龙鸣说唱。',
                    '· 非得这样说吗？我觉得吧，你也不要太硬！',
                    '· 无论在哪个世界，都有自己的法则和等价交换',
                    '· 沉溺于欲望的人，都会被欲望反噬。',
                '· 并不是所有表达爱意的方式，都会让人舒服']
                },
                {
                    img1:require('../assets/images2/five.png'),
                    title1:'健康一周汇',
                    title2:'专题区',
                    img2:require('../assets/images2/5.jpg'),
                    News:['· 中国人减寿因素，每一个都离你很近','· 这样揉耳朵，等于给全身做一套“养生操”',
                    '· 魏总是不舒服，需要做胃镜吗？','· 小年遇到大汉，非得这样说吗？',
                    '· 我今天就要给各位OG打个样，呼吸不止，说唱不停，我们是龙鸣说唱。',
                    '· 非得这样说吗？我觉得吧，你也不要太硬！',
                    '· 无论在哪个世界，都有自己的法则和等价交换',
                    '· 沉溺于欲望的人，都会被欲望反噬。',
                '· 并不是所有表达爱意的方式，都会让人舒服']
                }],
                optName:['实验室检查','科室检查','医技检查','专项检查'],
                optId:0,
                listName:['[乙肝两对半]','[丙肝检查]','[血常规]','[心肌功能]','[血脂]','[风湿检查]','[血液流边学检查]','[肝功能]',
                    '[糖尿病检测]','[胃功能]','[尿常规]','[微量元素检测]','[性激素]','[甲状腺功能化]']
            }
        },
        methods:{
            addClass: function (index) {
                this.optId = index;
            }
        }
    }
</script>

<style scoped>
.Main{
    min-width: 1200px;
    width: 100%;
    background-color: #ffffff;
     /*border: 1px solid red;*/
    margin-top: 4rem;
}
.Main .wrapper {
    width: 100%;
    padding: 2.5rem 8%;
    box-sizing: border-box;
    display: flex;
    justify-content: space-between;

}
 .Main .wrapper .content{
     width: 33.3%;
     display: flex;
     flex-direction: column;
     padding: 0 2rem;
     border-left: 1px solid #cccccc;
      /*border: 1px solid red;*/
 }
 .Main .wrapper .content:nth-of-type(1){
     border-left: none;
 }
    .Main .wrapper .content .top{
        width: 100%;
        height: 8rem;
        display: flex;
    }
    .Main .wrapper .content .top .logo{
        width: 20%;
        box-sizing: border-box;
        height: 100%;
        display: flex;
        padding-top: 1rem;
    }
    .top .logo img{
        height: 80%;
    }
    .Main .wrapper .content .top .title{
        width: 60%;
        height: 100%;
        display: flex;
        flex-direction: column;
    }
    .wrapper .content .top .title div:nth-of-type(1){
        height: 5rem;
        font-size: 2rem;
        color:#3a3a3a;
        line-height: 5rem;
        cursor: pointer;
    }
    .wrapper .content .top .title div:nth-of-type(2){
        height: 2rem;
        font-size: 1.4rem;
        color: #aaaaaa;
        line-height: 2rem;
        cursor: pointer;
    }
    .Main .wrapper .content .top .more{
        width: 20%;
        height: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 1.4rem;
        color: #3a3a3a;
        cursor: pointer;

    }
    .Main .wrapper .content .center{
        width: 100%;
        height: 12rem;
        border-bottom: #22aaff;
    }
    .wrapper .content .center img{
        width: 80%;
        height: 90%;
    }
    .Main .wrapper .content .bottom{
        width: 100%;
        flex: auto;
        display: flex;
        flex-direction: column;
    }
    .Main .wrapper .content .bottom .news{
        line-height: 3rem;
        width: 80%;
        overflow: hidden;
        text-overflow: ellipsis;
        display: flex;
        white-space: nowrap;

    }
    .Main .wrapper .content .bottom .news a{
        font-size: 1.4rem;
        color: #3a3a3a;
    }
    .tab{
        width: 100%;
        display: flex;
        flex: auto;
        justify-content: space-around;
    }
    .tab .opt{
        width: 30%;
        height: 100%;
        display: flex;
        flex-direction: column;
    }
    .tab .opt span{
        flex: 1;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: center;
        border-bottom: 1px dashed #cccccc;
        cursor: pointer;
        font-size: 1.6rem;
    }
    .tab .opt span.active{
        background-color: #22aaff;
        color: #ffffff;
    }
    .tab .optContent{
        width: 33rem;
        height: 100%;
    }
    .tab .optContent ul{
        width: 70%;
        height: 100%;
        display: flex;
        flex-wrap: wrap;
    }
    .tab .optContent ul li{
        flex: auto;
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 1.4rem;
    }




</style>
