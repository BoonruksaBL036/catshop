<template>
    <div class="container">
<div class="boxcontact">
    <img src="../image/logocatfoodshop.png" alt="">
    <div class="contact">
        <p><i class="pi pi-home"></i> 85 Village No. 3, Malaiman Road, Wang Taku Subdistrict, Mueang Nakhon Pathom District, Nakhon Pathom 73000</p>
        <p><i class="pi pi-envelope"></i> 664259036@webmail.npru.ac.th</p>
        <p><i class="pi pi-phone"></i> 0820070007</p>
    </div>
</div>
<div class="boxsocial">
    <div class="social"><i class="pi pi-facebook"></i></div>
    <div class="social"><i class="pi pi-instagram"></i></div>
    <div class="social"><i class="pi pi-twitter"></i></div>
</div>
    </div>
</template>

<script setup>
import 'primeicons/primeicons.css'
</script>

<style lang="scss" scoped>
.social{
    border-radius: 100%;
    width: 60px;
    height: 60px;
    background-color: #001839;
    display: flex;
    align-items: center;
    justify-content: center;
}
.social>i{
    color: white;
    font-size: 37px;
}
.boxsocial{
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 25px;
}
.contact{
    font-size: 20px;
    display: flex;
    flex-direction: column;
    align-items: start;
    justify-content: center;
}
.container{
    display: grid;
    grid-template-columns: repeat(2, minmax(0,1fr));
    padding: 0 15rem;
    background-color: #FEC600;
}
.boxcontact{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.boxcontact>img{
    width: 250px;
    height: auto;
}
</style>