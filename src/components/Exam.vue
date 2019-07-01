<template>
<div class="wrapper">
    <div class="exam">
        <ul>
            <li><a href="#">定制体检</a></li>
            <li><span>点击右侧开始</span></li>
        </ul>
        <ul>
            <li v-for="site in data"><a href="#"><img :src="site.img1" alt=""><span>{{site.title}}</span></a>
                <div><img :src="site.img2" alt=""></div>
            </li>
            <li><a href="#"><img src="../assets/images2/p9.png" alt=""><span>选择套餐</span></a></li>
        </ul>
    </div>
    <ul class="show">
        <li v-for="show in showData"><img :src="show.imgSrc" alt=""><span>{{show.slogan}}</span></li>
    </ul>
</div>
</template>

<script>
    export default {
        name: "Exam",
        data(){
            return{
                data:[{
                    img1:require('../assets/images2/p1.png'),
                    title:'开始评测',
                    img2:require('../assets/images2/13.png')
                },
                    {
                     img1:require('../assets/images2/p2.png'),
                     title:'基本信息',
                     img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p3.png'),
                        title:'健康状况',
                        img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p4.png'),
                        title:'饮食习惯',
                        img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p5.png'),
                        title:'运动习惯',
                        img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p6.png'),
                        title:'生活习惯',
                        img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p7.png'),
                        title:'完成评估',
                        img2:require('../assets/images2/13.png')
                    },
                    {
                        img1:require('../assets/images2/p8.png'),
                        title:'查看结果',
                        img2:require('../assets/images2/13.png')
                    }],
                showData:[
                    {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    },
                    {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    }, {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    }, {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    }, {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    }, {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    }, {
                        imgSrc:require('../assets/images2/1.jpg'),
                        slogan:'关爱父母'
                    },
                ]
            }
        }
    }
</script>

<style scoped>
.wrapper{
    box-sizing: border-box;
    padding: 0 10rem;
    width: 100%;
    min-width: 1200px;
}
.wrapper .exam {
    width:100%;
    background-color: #ffffff;
    margin: 1rem 0;
    display: flex;
}
    .exam ul:nth-child(1) {
        width: 15%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
    .exam ul:nth-child(1) li{
        margin-bottom: 2rem;
        padding: 2rem;

    }
    .exam ul:nth-child(1) li a{
        color: rgb(52,181,242);
        font-size: 2.4rem;
        font-weight: 500;
    }
   .exam ul:nth-child(1) li span{
       color: #a6a6a6;
       font-size: 1.2rem;
   }
 .exam ul:nth-child(2){
     width: 85%;
     display: flex;
     align-items: center;
     margin-left: 2rem;
 }
    .exam ul:nth-child(2) li{
        width: 11%;
        display: flex;
        align-items: center;
    }
    ul:nth-child(2) li:last-of-type a img{
        position: relative;
        width: 58%;
        top: 0;
        left: -1rem;
    }
    ul:nth-child(2) li a{
        flex-grow: 2;
       display: flex;
        flex-direction: column;
        align-items: center;
    }
    ul:nth-child(2) li a img{
        width: 100%;
    }
    ul:nth-child(2) li a span{
        font-size: 1.2rem;
        color: #a6a6a6;
    }
    ul:nth-child(2) li div{
        flex-grow: 1;
        text-align: center;
        transform: translateY(-1rem);
    }
    ul:nth-child(2) li div img{
        width: 50%;
    }
 .wrapper .show{
     width: 100%;
     margin-top: 3rem;
     display: flex;
 }
    .show li{
        position: relative;
        flex-grow: 1;
        /*border: 1px solid green;*/
        display: flex;
    }
    .show li:before{
        content: '';
        background-color: #000000;
        position: absolute;
        width: 100%;
        height: 100%;
        opacity: 0.4;
    }
    .show li img{
        width: 100%;
    }
    .show li span {
        position: absolute;
        display: inline-block;
        width: 3rem;
        left: 50%;
        top: 50%;
        transform: translateX(-50%);
        transform: translateY(-50%);
        font-size: 2.6rem;
        color: #ffffff;
    }


</style>
