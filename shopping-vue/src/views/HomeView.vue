<template>
   <div class="">

<div class="relative lg:mx-20">
  <img src="/base.png" alt="" class="object-cover w-full h-[700px]" />

  <div class="absolute inset-0 flex flex-col items-center justify-center text-center gap-5">
   <div class="text-2xl font-bold">New Collection</div>
<div class="text-4xl font-extrabold">The Gift Suite</div>
<div class="text-lg">Our latest collection of essential basics.</div>

  
    <button class="rounded-lg flex btn btn-neutral items-center gap-2 mt-4">
      Shop Now
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
        stroke-width="1.5" stroke="currentColor" class="size-6">
        <path stroke-linecap="round" stroke-linejoin="round"
          d="M17.25 8.25 21 12m0 0-3.75 3.75M21 12H3" />
      </svg>
    </button>
  </div>
</div>

<div class=" mt-20 flex flex-col items-center justify-center text-center gap-5 ">

  <div class="text-3xl font-extrabold">Shop The Collections</div>
  <div class="text-lg">Shop The Collections Shop the latest products from the most popular collections</div>

</div>

<div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6 mt-5 px-4">
  <div class="flex flex-col items-center justify-center text-center">
    <img class="rounded-full h-[200px]" src="/public/mens-ware.3ef0aeda7fd3efcbc351.jpg" alt="">
    <div class="text-lg font-bold mt-3">Men's wear</div>
  </div>
  <div class="flex flex-col items-center justify-center text-center">
    <img class="rounded-full h-[200px]" src="/public/ladies-ware.b5f7c2c84e90eda83610.jpg" alt="">
    <div class="text-lg font-bold mt-3">Ladies wear</div>
  </div>
    <div class="flex flex-col items-center justify-center text-center">
    <img class="rounded-full h-[200px]" src="/public/kids-ware.59e4ee050c8713a1871b.jpg" alt="">
    <div class="text-lg font-bold mt-3">Kids wear</div>
  </div>
    <div class="flex flex-col items-center justify-center text-center">
    <img class="rounded-full h-[200px]" src="/public/smart-watch.d359f83f8fa1f4111583.jpg" alt="">
    <div class="text-lg font-bold mt-3">Smart Watch</div>
  </div>
    <div class="flex flex-col items-center justify-center text-center">
    <img class="rounded-full h-[200px]" src="/public/sunglasses.7a154c200c3ff2218bc7.jpg" alt="">
    <div class="text-lg font-bold mt-3">Sunglasses</div>
  </div>
</div>

<div class=" mt-20 flex flex-col items-center justify-center text-center gap-5 ">

  <div class="text-3xl font-extrabold">New Arrival Products</div>
  <div class="text-lg">Shop the latest products from the most popular collections</div>

</div>

  <div class="mt-5 mx-20">
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :image="product.image"
      :name="product.name"
      :price="product.price"
    />
  </div>
  </div>

<div class="relative bg-primary mt-20">
  <img src="/base.png" alt="" class="object-cover w-full h-[400px]" />

  <div class="absolute inset-0 flex flex-col items-center justify-center text-center gap-5">

<div class="text-4xl font-extrabold text-white">End of Season Clearance</div>
<div class="text-4xl font-extrabold text-white">Sale upto 30%</div>

  
    <button class="rounded-lg flex btn btn-white text-primary items-center gap-2 mt-4">
      Shop Now
      <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
        stroke-width="1.5" stroke="currentColor" class="size-6">
        <path stroke-linecap="round" stroke-linejoin="round"
          d="M17.25 8.25 21 12m0 0-3.75 3.75M21 12H3" />
      </svg>
    </button>
  </div>
</div>
<Popular></Popular>

 </div>
  



</template>

<script>
import ProductCard from '@/components/ProductCard.vue';
import Popular from '@/components/Popular.vue';
import Navbar from '@/components/Navbar.vue';

export default {
  components: {
    ProductCard,
     Navbar,
    Popular,
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Black print T-shirt', price: 160, image:'/public/black-print-t-shirt.4caa3fc5cda7134848e4.jpg'},
        { id: 2, name: 'Fashion Shoes Sneaker', price: 200, image: '/public/fashion-shoes-sneaker.aab3c6439c42ef3bb22e.jpg' },
           { id: 3, name: 'Mens White Slip Shoes', price:120, image: '/public/men-white-espadrilles-slip-shoes.7d6c38ab10eeaec46100.jpg' },
              { id: 4, name: 'Ladies Luxurious Bag', price: 550, image: '/public/luxurious-bag.6a21a4817f9e60ad88f3.jpg' },
                 { id: 5, name: 'Ladies Green Top', price: 220, image: '/public/ladies-1.95e460073a09c4104eae.jpg' },
                    { id: 6, name: 'Ladies Onepiece Wear', price: 210, image: '/public/ladies-2.9d99f3dcc4ee05c39b09.jpg' },
                       { id: 7, name: 'Mens Brown Jacket', price: 600, image: '/public/mens-jecket.6f68430ae5803d37f883.jpg' },
        { id: 8, name: 'Sweater T-Shirt', price: 100, image: '/public/sweater-t-shirt.3aa23c5a167e8152f3f6.jpg' }
      ]
    };
  }
};
</script>

<style scoped>

</style>
