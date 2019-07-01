<template>
<div class="Promise">
    <div class="text">
        <h2>我们的承诺</h2>
        <p>我们可提供体检预约、报告解读、健康管理等服务。我们"推崇踏实、拼搏、责任"的企业精神，为您从检前到检后提供优质的服务，并做出以下承诺，让您放心预约。</p>
    </div>
    <ul class="show">
        <li v-for="pro in promiseData">
            <img :src="pro.imgSrc" alt="">
            <span>{{pro.name}}</span>
        </li>
    </ul>
</div>
</template>

<script>
    export default {
        name: "Promise",
        data(){
            return{
                promiseData:[
                    {
                        imgSrc:require('../assets/images2/p10.png'),
                        name:'官方授权'
                    },
                    {
                        imgSrc:require('../assets/images2/p11.png'),
                        name:'诚信承诺'
                    },
                    {
                        imgSrc:require('../assets/images2/p12.png'),
                        name:'低价承诺'
                    },
                    {
                        imgSrc:require('../assets/images2/p13.png'),
                        name:'检后服务'
                    },
                    {
                        imgSrc:require('../assets/images2/p14.png'),
                        name:'100%满意'
                    },
                    {
                        imgSrc:require('../assets/images2/p15.png'),
                        name:'90天退换'
                    }
                ]
            }
        }
    }
</script>

<style scoped>
    .Promise{
        min-width: 1200px;
        width: 100%;
        padding: 3rem 10rem;
        box-sizing: border-box;
        background-color: #ffffff;
    }
    .Promise .text{
        width: 60%;
        /*border: 1px solid red;*/
        margin: 0 auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 3rem;
    }
    .Promise .text h2{
        margin-bottom: 2rem;
        font-size: 2.4rem;
    }
    .Promise .text p{
        text-align: center;
        font-size: 1.6rem;
    }
    .Promise .show{
        width: 100%;
        /*border: 1px solid red;*/
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        margin-bottom: 2rem;
        /*border: 1px solid red;*/
    }
    .Promise .show li{
        width: 15%;
        height:100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .Promise .show li span{
        width: 80%;
        height: 20%;
        display: flex;
        align-items: center;
        justify-content: center;
        font-size: 1.6rem;
        font-weight: bold;
        color: #666666;
        padding-top: 1rem;
    }
    .Promise .show li img{
        width: 80%;
    }

</style>
