<template>
    <div>
        <div v-if="index==0">
           <GoodList :goodId="0"></GoodList>
        </div>
        <div v-if="index==1">
           <GoodList :goodId="1"></GoodList>
        </div>
        <div v-if="index==2">{{index}}</div>
        <div v-if="index==3">{{index}}</div>
        <div v-if="index==4">{{index}}</div>
        <div v-if="index==5">{{index}}</div>
        <div v-if="index==6">{{index}}</div>
    </div>
</template>
 <script>
import Msg from './msg'
import GoodList from './GoodList'
export default {
    data(){
        return{
            index:0
        }
    },
    mounted:function(){
        var obj=this
        Msg.$on('val',function(response){
            obj.index=response
        })
    },
    components:{
        GoodList
    }
}
</script>