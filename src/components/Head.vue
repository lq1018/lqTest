<template>
    <div class="Head">
        <ul class="headLeft">
            <li><a href="#">预约平台</a></li>
        </ul>
        <ul class="headRight">
            <li v-for="site in sites"><a href="#"><img :src="site.imgSrc" alt="">{{site.name}}</a></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "Head",
        data(){
            return {
                sites:[
                    {
                        name:'请登录',imgSrc:require('../assets/images2/tu5.png')
                    },
                    {
                        name:'【免费注册】',
                    },
                    {
                        name:'体验卡登录',imgSrc:require('../assets/images2/tu1.png')
                    },
                    {
                        name:'客户服务',imgSrc:require('../assets/images2/tu2.png')
                    },
                    {
                        name:'网站导航',imgSrc:require('../assets/images2/tu3.png')
                    }
                ]
            }
        },

    }
</script>

<style scoped>
    .Head{
        position: relative;
        box-sizing: border-box;
        width: 100%;
        height: 40px;
        padding: 0 100px;
        background: #dddddd;
    }
    .Head .headLeft{
        display: inline-block;
        height: 100%;
        width: 200px;
    }
    .headLeft li a{
        height: 40px;
        line-height: 40px;
        color: #333333;
        font-size: 16px;
    }
    .Head .headRight{
        display: inline-block;
        position: absolute;
        right: 100px;
    }
    .headRight li{
        float: left;
        margin-left: 20px;
    }
    .headRight li a{
        display: inline-block;
        height: 40px;
        line-height: 40px;
        color: #333333;
        font-size: 16px;
        padding: 0 10px;
    }
    .headRight li a img{
        display: inline-block;
        margin-right: 10px;
    }
</style>
