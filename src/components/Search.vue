<template>
 <div class="search">
     <div class="logo"><img src="../assets/images2/1.png" alt=""></div>
     <div class="city">福州 <a href="#">[更换]</a></div>
     <div class="searchInp">
         <ul>
             <li :class=" this.lock ? 'active': ''" v-on:click="tab1">搜套餐</li>
             <li :class="this.lock ? ' ' : 'active'" v-on:click="tab2">选医院</li>
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
            tab1: function () {
               this.lock= true;
               if(this.lock==true){
                   this.placeholder='请输入你要搜索的套餐'
               }
            },
            tab2:function () {
                this.lock = false;
                if(this.lock==false){
                    this.placeholder='请输入你要选择的医院'
                }
            }

        }
    }
</script>

<style scoped>
.search{
    min-width: 1200px;
    position: relative;
    width: 100%;
    box-sizing: border-box;
    padding: 0 10rem;
    margin-bottom: 2rem;
}
.search .logo{
    position: relative;
    display: inline-block;
    width: 8rem;
    margin-top: 2rem;
    left: -1.5rem;
}
.search .logo img{
    width: 100%;
}
.search .city{
    position: absolute;
    border: 1px solid #cccccc;
    padding: 0.5rem 1rem;
    left: 30rem;
    top: 5rem;
    font-size: 1.4rem;
    font-weight: bold;
}
.search .city a{
    font-size: 1.4rem;
    color: #666666;
    font-weight: normal;
}
.search .searchInp{
    display: inline-block;
    position: absolute;
    width: 30rem;
    top: 2rem;
    left: 45rem;
}
.search .searchInp ul li{
    width: 6rem;
    display: inline-block;
    border: 1px solid #dddddd;
    border-bottom: none;
    text-align: center;
    padding: 0.7rem 0.7rem;
    cursor: pointer;
    margin-right: 0.5rem;
    font-size: 1.3rem;
    font-weight: bold;
}
.search .searchInp ul li.active{
    background-color: #22aaff;
    color: #ffffff;
}
.search .searchInp input{
    width: 30rem;
    height: 3.5rem;
    text-indent: 1rem;
    border: 1px solid #22aaff;
}
.search .searchInp .soso{
    display: inline-block;
    position: absolute;
    height: 3.5rem;
    width: 8rem;
    background-color: #22aaff;
    text-align: center;
    line-height: 3.5rem;
    top:3rem;
    left: 30rem;
    color: #ffffff;
    font-size: 1.4rem;
    cursor: pointer;
    font-weight: bold;
}
</style>
