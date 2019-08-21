<template>
    <div class="page four">
        <Header>
            <template v-slot:header="props">
                <p class="header-h2">{{props.icon}}</p>
            </template>
        </Header>
        <h1>four</h1>
    </div>
</template>

<script>
import Header from "../header";
export default {
    components:{
        Header
    }
}
</script>

<style>
.header-h2{
    position: absolute;
    left: .2rem;
    top: .2rem;
    font-size: .8rem;
    color: aliceblue;

    }
</style>


