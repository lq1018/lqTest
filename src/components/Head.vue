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
        min-width: 1200px;
        padding: 0 10rem;
        background: #dddddd;
    }
    .Head .headLeft{
        display: inline-block;
        width: 20rem;
    }
    .headLeft li a{
        line-height: 4rem;
        color: #333333;
        font-size: 1.6rem;
    }
    .Head .headRight{
        display: inline-block;
        position: absolute;
        right: 10rem;
    }
    .headRight li{
        float: left;
        margin-left: 2rem;
    }
    .headRight li a{
        display: inline-block;
        line-height: 4rem;
        color: #333333;
        font-size: 1.6rem;
        padding: 0 1rem;
    }
    .headRight li a img{
        display: inline-block;
        margin-right: 1rem;
    }
</style>
