<template>
    <div class="main">
        <div class="left">
            <Left></Left>
        </div>
        <div class="right">
            <div class="top">
                <img src="../../public/img/title.png">
            </div>
            <div class="buttom">
                <Right></Right>
            </div>
        </div>
    </div>
</template>
<script>
// 组件引入
import Left from '../components/Left.vue'
import Right from '../components/Right.vue'
export default {
    name:"Index",
    // 组件注册
    components:{
        Left,
        Right
    }
    
}
</script>
<style type="text/css">
/* 设置所有默认间距为0，各浏览器的默认不一致 */
    *{
        padding:0;
        margin:0;
     }
     .left{
         width:100px;
         float:left;
         margin-right: 10px;
     }
     .right{
         width:1000px;
         float:left;
         margin-left:10px;
     }
     .main{
         /* 设置宽度为了居中，没有宽度不能居中 */
         width:1200px; 
         margin:20px auto;
     }
     .top{
         margin-bottom: 20px;;
     }
     .top img{
         height:220px;
         width:1000px;
     }
     .left,.right{
         background-color:#f5f5f5;
         height:640px;
     }
</style> 
