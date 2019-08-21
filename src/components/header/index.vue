<template>
    <div class="header">
        <slot name="header" :icon="icon"></slot>
        <h2>{{title}}</h2>
    </div>
</template>

<script>
export default {
    name:"header",
    data(){
        return{
            title:"猫眼电影",
             icon:"<",
        }
    }
}
</script>

<style>
    .header{
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        width: 100%;
        height: 1.5rem;
        justify-content: center;
        align-items: center;
        background: red;
    }
    .header>h2{
        color: aliceblue
    }
</style>


