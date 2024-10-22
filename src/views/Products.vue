<template>
    <div class="container">
        <div class="cover">
            <div class="box-logo">
                <img src="../image/logocatfoodshop.png" />
                <h1 class="title">Products</h1>
            </div>
            
            <div class="box-item">
                <Item :product="productList"/>
            </div>
        </div>
    </div>
</template>

<script setup>
import product from "../assets/products/products.json"
import Item from "../components/Item.vue";

const productList = product.products.filter(item => (item.id))
// export default {
//   name: 'Products',
// }
</script>

<style lang="scss" scoped>
.box-logo{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
}
.box-logo>img{
    position: absolute;
    bottom: 0.1rem;
    transform: translateX(61px);
    width: 150px;
}
.title{
    font-size: 60px;
}

.container{
    padding: 0 10rem;
}
.cover{
    background-color: white;
    padding: 10rem 2rem;
    display: flex;
    flex-direction: column;
    gap: 5rem 0;
}
.box-item{
    display: grid;
    grid-template-columns: repeat(4, minmax(0, 1fr));
    gap: 50px 25px;
}
</style>