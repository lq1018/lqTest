<template>
<div class="about">
<ul class="abCon">
    <li v-for="abdata in abData">
        <h3>{{abdata.title}}</h3>
        <div class="Item">
            <p v-for="listName in abdata.listName">{{listName}}</p>
        </div>
    </li>
</ul>
</div>
</template>
<script>
export default {
    name:'About',
    data(){
        return{
            abData:[
                {
                    title:'合作伙伴',
                    listName:['平安健康网','健康卫士']
                },{
                    title:'预约保障',
                    listName:['用户协议','真实评价','隐私声明']
                },{
                    title:'常见问题',
                    listName:['新手指南','会员特权说明','优惠券使用说明','E卡/金卡说明','E卡/金卡使用流程']
                },{
                    title:'帮助信息',
                    listName:['网站地图','招贤纳士','品牌招商','纠纷维权']
                },{
                    title:'关于我们',
                    listName:['平台简介','媒体报道','联系我们','我们的团队','版权声明']
                }
            ]
        }
    }
}
</script>
<style scoped>
.about{
    min-width: 1200px;
    width: 100%;
    height: 25rem;
    box-sizing: border-box;
    padding: 3rem 10rem;
    background-color: #ffffff;
}
.about .abCon{
    width: 100%;
    height: 100%;
    display: flex;
}
.about .abCon li{
   width: 15%;
   height: 100%;
   /* border:1px solid red; */
   display: flex;
   flex-direction: column;
}
.abCon li h3{
    width: 100%;
    font-size: 1.6rem;
    font-weight: bold;
    height: 25%;
    text-align: center;
}
.abCon li .Item{
    width: 100%;
    height: 75%;
    margin-top: 1.5rem;
    text-align: center;
}
.abCon li .Item p{
    font-size: 1.4rem;
    color: #666666;
    padding-top: 0.5rem;
}

</style>
