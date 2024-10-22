<template>
    <div class="container">
        <div class="content">        
            <div class="box-image">
                <img src="../image/logocatfoodshop.png" alt="" class="image">
            </div>
        <ul class="menu">
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="/products">Products</router-link></li>
            <li><router-link to="/brand">Brand</router-link></li>
        </ul>
        </div>
        <div class="">
<i class="pi pi-search"></i>
        </div>
    </div>
</template>

<script setup>
import 'primeicons/primeicons.css'
import router from '../router/index.vue';
</script>

<style lang="scss" scoped>
.container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #FEC600;
    overflow: hidden;
    height: 10rem;
}
.content{
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.menu{
    display: flex;
    justify-content: space-between;
    align-items: center;
    list-style: none;
    margin-left: 25px;
}
.menu>li{
    font-size: 18px;
    margin-left: 50px;
}
.menu>li>a{
    text-decoration: none;
    color: black;
}
.image{
    width: 100%;
    height: 100%;
}
.box-image{
    height: 10rem;
    width: 100%;
}

</style>