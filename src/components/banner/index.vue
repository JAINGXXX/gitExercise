<template>
    <div class="banner">
        <div class="swiper-container imgsOne" ref="banner">
             <slot name="banner" :contents="arr"></slot>
        </div>
    </div>
</template>

<script>
import Swiper from "swiper";
import 'swiper/dist/css/swiper.css'
export default {
    name:"banner",
    data(){
        return {
            arr:["http://a.hiphotos.baidu.com/lvpics/h=800/sign=2d496375d739b60052ce02b7d9513526/a6efce1b9d16fdfa97d6a678b68f8c5495ee7be9.jpg",
            "http://pic37.nipic.com/20140113/8800276_184927469000_2.png",
            "http://pic.58pic.com/58pic/15/02/65/67d58PICkMZ_1024.jpg",
            "http://pic62.nipic.com/file/20150318/8684504_093611837474_2.jpg"
            ]
        }
    },
      mounted(){
        new Swiper(this.$refs.banner,{
            autoplay: {
           disableOnInteraction: false
        },
        loop:true,
         pagination: {
           el: '.swiper-pagination',
    },
    }
        )
     }
}
</script>

<style>

</style>


