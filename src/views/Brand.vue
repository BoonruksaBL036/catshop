<template>
    <div class="container">
        <div class="cover">
            <div class="box-logo">
                <img src="../image/logocatfoodshop.png" />
                <h1 class="title">Brand</h1>
            </div>

            <div class="container-content">
                <router-link to="/Nekko"  class="cir-brand">
                    <img src="../image/nekko.png" />
                </router-link>
                <router-link to="/" class="cir-brand">
                    <img src="../image/logomeo.png" />
                </router-link>
                <router-link to="/" class="cir-brand">
                    <img src="../image/kanivalogo.jpg" />
                </router-link>
                <router-link to="/" class="cir-brand">
                    <img src="../image/logowhiskas.jpg" />
                </router-link>
                <router-link to="/" class="cir-brand">
                    <img src="../image/royal.png" />
                </router-link>
                <router-link to="/" class="cir-brand">
                    <img src="../image/purina.png" />
                </router-link>
            </div>
        </div>
    </div>
</template>

<script setup>

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
    bottom: -0.2rem;
    transform: translateX(7px);
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
    padding: 5rem 2rem;
    display: flex;
    flex-direction: column;
}

.container-content{
    display: grid;
    grid-template-columns: repeat(3, minmax(0, 1fr));
    padding: 5rem 10rem;
    justify-content: center;
    align-items: center;
    gap: 25px;
}

.cir-brand{
    display: flex;
    justify-content: center;
    align-items: center;
}
.cir-brand>img{
    border-radius: 100%;
    overflow: hidden;
    width: 180px;
    height: 180px;
    object-fit: cover;
}

</style>