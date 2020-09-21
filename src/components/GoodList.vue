<template>
    <div class="show">
        <ul class="goodList">
            <li v-for="(item,index) in list" :key=index>
                <img :src="item.img">
                <p>{{item.goodsName}}</p>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name:"show",
    data(){
        var obj=this;
        this.$axios.get("json/cake.json").then(function(res){
            obj.list=res.data;
        })
        return{
            list:[]
        }
    },
    props:{
        goodId:Number
    },
    watch:{
        goodId(){
            var obj=this;
            var url="";
            if(obj.goodId==0){
                url="json/cake.json";
            }else if(obj.goodId==1){
                url="json/milkTea.json";
            }
            this.$axios.get(url).then(function(res){
            obj.list=res.data;
        })
        return{
            list:[]
        }
        }
    }
}
</script>
<style>
.goodList li{
    width:200px;
    height:200px;
    list-style: none;
    float:left;
    font-size:9px;
    margin-bottom: 20px;;
}
.goodList img{
    width:180px;
    height:150px;
}
</style>