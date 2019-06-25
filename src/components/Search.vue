<template>
 <div class="search">
     <div class="logo"><img src="../assets/images2/1.png" alt=""></div>
     <div class="city">福州 <a href="#">[更换]</a></div>
     <div class="searchInp">
         <ul>
             <li :class=" this.lock ? 'active': ''" v-on:click="tab">搜套餐</li>
             <li :class="this.lock ? ' ' : 'active'" v-on:click="tab">选医院</li>
         </ul>
         <div>
             <input type="text" :placeholder="placeholder">
         </div>
         <div class="soso">搜索</div>
     </div>
 </div>
</template>

<script>
    export default {
        name: "Search",
        data(){
            return{
                lock:true,
                placeholder:'请输入你要搜索的套餐'
            }
        },
        methods: {
            tab: function () {
               this.lock= this.lock?false:true;
               if(this.lock==true){
                   this.placeholder='请输入你要搜索的套餐'
               }else {
                   this.placeholder='请输入你要选择的医院'
               }
            }

        }
    }
</script>

<style scoped>
.search{
    position: relative;
    width: 100%;
    height: 120px;
    box-sizing: border-box;
    padding: 0 100px;
}
.search .logo{
    position: relative;
    display: inline-block;
    width: 80px;
    height: 80px;
    margin-top: 20px;
    left: -15px;
}
.search .city{
    position: absolute;
    border: 1px solid #cccccc;
    padding: 5px 10px;
    left: 300px;
    top: 50px;
    font-size: 14px;
    font-weight: bold;
}
.search .city a{
    font-size: 14px;
    color: #666666;
    font-weight: normal;
}
.search .searchInp{
    display: inline-block;
    position: absolute;
    width: 300px;
    height: 90px;
    top: 20px;
    left: 450px;
}
.search .searchInp ul li{
    width: 60px;
    height: 20px;
    display: inline-block;
    border: 1px solid #dddddd;
    border-bottom: none;
    text-align: center;
    padding: 5px 7px;
    cursor: pointer;
    margin-right: 5px;
}
.search .searchInp ul li.active{
    background-color: #22aaff;
    color: #ffffff;
}
.search .searchInp input{
    width: 300px;
    height: 30px;
    text-indent: 10px;
    border: 1px solid #22aaff;
}
.search .searchInp .soso{
    display: inline-block;
    position: absolute;
    height: 34px;
    width: 80px;
    background-color: #22aaff;
    text-align: center;
    line-height: 34px;
    top:30px;
    left: 300px;
    color: #ffffff;
    font-size: 14px;
    cursor: pointer;
}
</style>
