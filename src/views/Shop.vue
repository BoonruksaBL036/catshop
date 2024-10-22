<template>

    <div class="container">
        <div class="cover">
            <div class="box-logo">
                <img src="../image/logocatfoodshop.png" />
                <h1 class="title">Shop</h1>
            </div>

            <div class="cover-content">
                <div v-for="item in product" class="box-item">
                    <diV class="container-image">
                        <div class="box-image">
                            <img :src="`/src/image/${item.image}`" />
                        </div>
                        <div class="subimage">
                            <div v-for="i in 3">
                                <img :src="`/src/image/${item.image}`" class="cover-image">
                            </div>
                        </div>
                    </diV>
                    <div class="content">
                        <div>
                            <h1 class="title-des">{{ item.name }} {{ item.description }}</h1>
                            <!-- line -->
                            <div class="line"></div>
                        </div>
                        <div class="price">
                            <h1>{{ item.price }} ฿</h1>
                        </div>
                        <div class="sub-bottom">
                            <p>สอบถามสั่งซื้อได้ที่ @LINE</p>
                            <button><i class="pi pi-instagram"></i>Chat & Shop</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

</template>

<script setup>
import productList from '../assets/products/products.json';
import { useRoute } from 'vue-router';

const route = useRoute();
const id = route.params.id;

const product = productList.products.filter(item => (item.id == Number(id)));
</script>

<style lang="scss" scoped>
.box-logo {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
}

.box-logo>img {
    position: absolute;
    bottom: -0.7rem;
    transform: translateX(40px);
    width: 150px;
}

.title {
    font-size: 60px;
}

.container {
    padding: 0 10rem;
}

.cover {
    background-color: white;
    height: 40rem;
    padding: 4rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 2rem 0;
}

.cover-content {
    // padding: 0 50rem;
    display: flex;
    gap: 5rem 0;
    justify-content: center;
}

.box-item {
    display: flex;
}

.content {
    margin-left: 5rem;
}

.container-image{
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 17px;
}

.box-image {
    width: 200px;
    height: 260px;
    display: flex;
    flex-direction: column;
    align-items: center;
    box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1);
}

.box-image>img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.subimage {
    display: flex;
}

.cover-image {
    width: 90px;
}

.line {
    width: 50px;
    height: 1px;
    background-color: #808080;
}

.price {
    border-bottom: 1px solid #808080;
}

.sub-bottom>button {
    display: flex;
    font-weight: bold;
    gap: 5px;
    border: 0;
    background-color: #00e11f;
    color: white;
    padding: 10px 20px;
    border-radius: 10px;

}

.title-des {
    width: 50vw;
}
</style>