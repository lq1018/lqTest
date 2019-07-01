<template>
<div class="pec">
    <div class="pec-nav">
        <ul>
            <li><span>热门</span>体检中心</li>
        </ul>
        <ul>
            <li><a class="active" href="#">公立三甲</a></li>
            <li><a href="#">专业体检中心</a></li>
            <li><a href="#">公立医院</a></li>
            <li><a href="#">民营医院</a></li>
            <li><a href="#">更多</a></li>
        </ul>
    </div>
    <div class="pec-content">
        <ul v-for="content in conData">
            <li><img :src="content.img1" alt=""></li>
            <li>
                <div>套餐：{{content.tcMount}} 评价：{{content.pjMount}}</div>
                <div><img src="../assets/images2/tu6.png" alt="">公立三甲</div>
            </li>
            <li><a href="#">{{content.hosName}}</a></li>
        </ul>
    </div>
</div>
</template>

<script>
    export default {
        name: "Pec",
        data(){
            return{
                navData:['公立三甲','专业体检中心','公立医院','民营医院'],
                conData:[
                    {
                        img1:require('../assets/images2/2.jpg'),
                        tcMount:23,
                        pjMount:169,
                        hosName:'福建省人民医院体检中心(福建中医药大学第一附属医院)'
                    },{
                        img1:require('../assets/images2/2.jpg'),
                        tcMount:58,
                        pjMount:119,
                        hosName:'福建医科大学附属第一医院体检中心'
                    },{
                        img1:require('../assets/images2/2.jpg'),
                        tcMount:12,
                        pjMount:149,
                        hosName:'福建中医药大学附属福州中医院体检中心'
                    },{
                        img1:require('../assets/images2/2.jpg'),
                        tcMount:52,
                        pjMount:129,
                        hosName:'福建省人民医院体检中心(福建中医药大学第一附属医院分解机覅诶房间诶)'
                    }
                ]
            }
        }
    }
</script>

<style scoped>

.pec{
    min-width: 1200px;
    width: 100%;
    padding: 0 10rem;
    box-sizing: border-box;
}
    .pec .pec-nav{
        width: 100%;
        margin-top: 3rem;
        background-color: #ffffff;
        display: flex;
    }
    .pec .pec-nav ul:nth-child(1){
        flex-grow: 2;
    }
    .pec-nav ul:nth-child(1) li{
        box-sizing: border-box;
        width: 100%;
        line-height: 6rem;
        padding-left: 2rem;
        font-size: 2.4rem;
        color: #3a3a3a;
    }
    .pec-nav ul:nth-child(1) li span{
               color: #22aaff;
    }
    .pec .pec-nav ul:nth-child(2){
        flex-grow: 8;
        display: flex;
        justify-content: flex-end;
    }
    .pec-nav ul:nth-child(2) li{
        display: flex;
        align-items: center;
        margin: 0 1rem;
        padding: 0 1.5rem;
        font-size: 1.4rem;
        font-weight: bold;
    }
    .pec-nav ul:nth-child(2) li:last-of-type{
        border-left: 1px solid #dddddd;
    }
    ul:nth-child(2) li a{
        width: 100%;
        padding: 0.5rem 1rem;
        text-align: center;
        border-radius: 0.5rem;
        color:#666666;
    }
    ul:nth-child(2) li a.active{
          background-color: #22aaff;
        color: #ffffff;
        border-radius: 0.5rem;
    }
    .pec .pec-content{
        width: 100%;
        margin-top: 3rem;
        display: flex;
        justify-content: space-between;
    }
    .pec-content ul{
        width: 23%;
        border: 1px solid green;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
    }
    .pec-content ul li:nth-of-type(2) {
        box-sizing: border-box;
        width: 100%;
        padding: 0.5rem 1rem;
        display: flex;
        justify-content: space-between;
        border-bottom: 1px solid #dddddd;
    }
    ul li:nth-of-type(2) div{
        font-size: 1.2rem;
        color: #666666;
    }
    .pec-content ul li:nth-of-type(1) img{
        width: 100%;
    }
   .pec-content ul li:nth-of-type(3){
        box-sizing: border-box;
        width: 100%;
        line-height: 4rem;
        padding: 0 1.5rem;
        overflow: hidden;
        text-overflow: ellipsis;
         white-space: nowrap;
    }
   .pec-content ul li:nth-of-type(3) a{
        color: #666666;
        font-size: 1.6rem;
    }
</style>
