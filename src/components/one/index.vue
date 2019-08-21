<template>
    <div class="page one">
        <Header/>
        <Banner>
            <template v-slot:banner="props">
                    <div class="swiper-wrapper">
                            <div class="swiper-slide" 
                                v-for="(item,index) in props.contents"
                                :key="index"
                                ><img :src="item" alt="">      
                            </div>
                    </div>
                 <div class="swiper-pagination"></div>
            </template>
        </Banner>
    </div>
</template>

<script>
import Header from "../header";
import Banner from "../banner";
export default {
    components:{
        Header,
        Banner
    },
    created(){
        console.log(this.Banner)
    },
}
</script>

<style>
.imgsOne{
    width: 100%;
    height: 5rem;
    overflow: hidden;
}
.imgsOne>.swiper-wrapper{
    width: 100%;
    height: 100%;
}
.imgsOne>.swiper-wrapper>.swiper-slide{
    width: 100%;
    height: 100%;
}
.imgsOne img{
    width: 100%;
    height: 5rem;
    background-size: cover;
}
</style>


