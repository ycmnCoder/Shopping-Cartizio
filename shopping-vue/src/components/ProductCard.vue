<template>
  <div class="max-w-sm rounded overflow-hidden">
    <div class="relative">
    <img class="w-full h-100 object-cover border border-gray-200" :src="image" alt="" />
    <button class="btn btn-primary absolute bottom-0 w-full" @click="addToCart()">Add to Cart</button>
  </div>
  <div>
    <div class="py-4">
      <div class="font-bold text-xl mb-2">{{ name }}</div>
      <p class="text-gray-700 text-base">
        ${{ price }}
      </p>
    </div>
  </div>
  </div>
</template>

<script>
export default {
  
  props: {
    image: {
      type: String,
      required: true
    },
    name: {
      type: String,
      required: true
    },
    price: {
      type: Number,
      required: true
    },
  },
 methods: {
 addToCart() {
  const existingCart = JSON.parse(localStorage.getItem('cart')) || [];

  const newItem = {
    name: this.name,
    price: this.price,
    image: this.image
  };

  existingCart.push(newItem);
  localStorage.setItem('cart', JSON.stringify(existingCart));


  if (window.cartCountUpdater) {
    window.cartCountUpdater();
  }

  this.$router.push('/cart');
}


}
      }

</script>

<style scoped>

</style>
