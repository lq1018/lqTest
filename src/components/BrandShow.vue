<template>
    <div class="brand">
     <div class="text">
         <h2>长期合作伙伴</h2>
         <p>我们以诚信、共赢、开创的经营理念，与全国数百家公立/三甲/专业体检中心建立的长期稳定的合作关系，为您创造良好的体验环境，完善的技术，和周到的预约服务。</p>
     </div>
        <ul class="show">
            <li v-for="img in imgSrc"><img :src="img" alt=""></li>
        </ul>
    </div>
</template>

<script>
    export default {
        name: "BrandShow",
        data(){
            return{
                imgSrc:[require('../assets/images2/10.png'), require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/10.png'),
                    require('../assets/images2/10.png'),require('../assets/images2/10.png'),
                    require('../assets/images2/10.png'),require('../assets/images2/10.png'),
                    require('../assets/images2/10.png'),require('../assets/images2/10.png'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg'),require('../assets/images2/11.jpg'),
                    require('../assets/images2/11.jpg')
                ]
            }
        }
    }
</script>

<style scoped>
.brand{
    min-width: 1200px;
    width: 100%;
    padding: 3rem 10rem;
    box-sizing: border-box;
}
.brand .text{
    width: 60%;
    /*border: 1px solid red;*/
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 3rem;
}
.brand .text h2{
    margin-bottom: 2rem;
    font-size: 2.4rem;
}
    .brand .text p{
        text-align: center;
        font-size: 1.6rem
    }
 .brand .show{
     width: 100%;
     /*border: 1px solid red;*/
     display: flex;
     justify-content: space-between;
     flex-wrap: wrap;
     margin-bottom: 2rem;
 }
    .brand .show li{
        width: 13%;
        margin-bottom: 1rem;
    }
    .brand .show li img{
        width: 100%;
    }
</style>
