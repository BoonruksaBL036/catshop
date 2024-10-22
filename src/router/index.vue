<script>
import { createRouter, createWebHistory } from 'vue-router'
import Home from '../views/Home.vue';
import Products from '../views/Products.vue';
import Shop from '../views/Shop.vue';
import Brand from '../views/Brand.vue';
import Nekko from '../views/Nekko.vue';
// import About from '@/views/About.vue'

const routes = [
{
    path: '/',
    name: 'Home',
    component: Home,
  },
  {
    path: '/products',
    name: 'Products',
    component: Products,
  },
  {
    path: '/products/shop/:id',
    name: 'Shop',
    component: Shop,
  },
  {
    path: '/brand',
    name: 'Brand',
    component: Brand,
  },
  {
    path: '/Nekko',
    name: 'Nekko',
    component: Nekko,
  }

//   {
//     path: '/about',
//     name: 'About',
//     component: About,
//   },
]

const router = createRouter({
  history: createWebHistory(),
  routes,
})

export default router
</script>