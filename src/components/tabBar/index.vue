<template>
    <div class="footer">
        <ul>
            <li v-for="(item,index) in lists" :key="index" @click="handleTabBar(index)"
            :class="catIndex==index?'colors':''"
            >{{item}}</li>
        </ul>
    </div>
</template>

<script>
import { constants } from 'crypto';
export default {
    name:"tabBar",
    data(){
        return{
            lists:["首页","列表","订单","我的"],
            catIndex :"0"
        }
    },
    created(){
        console.log(this.list)
    },
    methods:{
        handleTabBar(index){
            this.catIndex = index;
            this.$emit("handleTab",index)
        }
        
    }
}
</script>

<style>
   .footer{
       position: fixed;
       bottom: 0;
       left: 0;
       width: 100%;
       height: 1.5rem;
       border-top: 1px solid #ccc
   }
   .footer>ul{
       display: flex;
       width: 100%;
       height: 100%;
       justify-content: space-between;
   }
   .footer>ul>li{
       display: flex;
        width: 100%;
       height: 100%;
       justify-content: center;
       align-items: center;
   }
   .colors{
       color: red;
   }
</style>


