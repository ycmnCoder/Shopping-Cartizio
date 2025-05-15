<template>
  <div class=" mx-0 lg:mx-20 my-20">
    <h1 class="text-3xl font-bold mb-4">Fashion</h1>

    <div class="flex font-semibold">
        <a href="/" class="">CARTZIO ></a>
        <div class="text-primary">  SHOPCART</div>


    </div>

    <div class=" mt-10 p-4 bg-gray-100 shadow rounded flex items-center font-bold  "> 
        <div>Product/Name/Price</div>
        <!-- <div class=" xl:ml-[430px]">Name</div>
        <div class=" xl:ml-[400px]">Price</div> -->
        <div></div>
    </div>

    <div v-if="cart.length">
<div v-for="(item, index) in cart" :key="index" class="my-4 p-4 rounded shadow mx-auto w-full  flex flex-col items-center md:flex-row  md:justify-between">
    <img :src="item.image" alt="" class="w-24 h-24 object-cover mb-4 md:mb-0" />
    
        <p class="font-semibold">{{ item.name }}</p>
        <p>${{ item.price }}</p>
    
    <div class="p-5 cursor-pointer" @click="removeItem(index)">
        <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="size-6">
            <path stroke-linecap="round" class="text-primary" d="M6 18 18 6M6 6l12 12" />
        </svg>
    </div>
</div>



      
      <div class="mt-6 text-xl font-bold p-4 rounded shadow max-w-[300px] flex justify-between">
        <div class="text-primary">TOTAL:</div>
        <div> ${{ totalPrice }}</div>

      </div>
    </div>

    <div v-else>
      
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cart: [],
      totalPrice: 0
    };
  },
  mounted() {
    this.loadCart();

  },
  methods: {
   
    loadCart() {
      const savedCart = localStorage.getItem('cart');
      this.cart = savedCart ? JSON.parse(savedCart) : [];
      this.calculateTotal();
    },

    
    calculateTotal() {
      this.totalPrice = this.cart.reduce((sum, item) => sum + Number(item.price), 0);
    },

   
    removeItem(index) {
      this.cart.splice(index, 1); 
      localStorage.setItem('cart', JSON.stringify(this.cart)); 
      this.calculateTotal();
      if (window.cartCountUpdater) {
      window.cartCountUpdater();
    }

    }
    
  }
};
</script>
