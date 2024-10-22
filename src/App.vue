<template>
  <div class="yommix">
  <Header class="Header"/>
  <!-- <div>
    <div class="SuperL">
      <img src="./image/superL.png" alt="">
    </div> -->

  <!-- </div> -->
   <router-view />
  <Footer /> 
</div>
</template>

<script setup>
import Footer from './components/Footer.vue';
import Header from './components/Header.vue';


</script>

<style lang="scss" scoped>
.SuperL{
  margin: 0;
}
.Header{
  padding: 0 10rem;
}
.yommix{
  background-color: #FEC600;
}
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>