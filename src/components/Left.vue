<template>
    <div class="sleft">
        <div class="title">热门推荐</div>
        <ul class="menu">
            <li v-for="(item,index) in goodsList" :key="index" @click="menu(index)">{{item}}</li>
        </ul>
    </div>
</template>
<script>
import Msg from './msg'
export default {
    data(){
        return{
            goodsList:["蛋糕","奶茶","牛奶","可乐","薯片","牛肉干","辣条"]
        }
    },
    methods:{
        menu(index){
            Msg.$emit("val",index)
        }
    }
}
</script>
<style>
    .title{
        width:100px;
        color:red;
    }
    .sleft{
        padding: 50px 0;
    }
    .menu li{
        list-style: none;
        height:70px;  
        margin-bottom: 3px;
        background-color: white;
        line-height: 70px; 
        /* line-height和height相同，文字行内居中 */
        cursor: pointer;
    }
</style>