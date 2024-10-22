<template>
        <div class="container" v-for="item in product" :key="item.id">
            <div class="box-image">
                <img :src="`/src/image/${item.image}`" alt="">
            </div>
            <h1>{{ item.name }}</h1>
            <p class="text-price">{{item.price}} B</p>
            <router-link :to='`/products/shop/${item.id}`'>
                <button class="btn">
                    shop
                </button>
            </router-link>
        </div>
</template>

<script setup>

const props = defineProps(["product"]);
</script>

<style lang="scss" scoped>
.text-price{
    font-size: 18px;
}
.container{
    display:flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
    padding: 10px;
}
.btn{
    background-color: #FEC600;
    padding: 10px 20px;
    border: 0;
    border-radius: 10px;
}
.box-image{
    width: 123px;
    height: 162px;
    display: flex;
    justify-content: center;
    align-items: center;
}
.box-image>img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}

</style>