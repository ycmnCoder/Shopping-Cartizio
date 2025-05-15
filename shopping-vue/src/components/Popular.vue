<template>
  <div class="flex flex-col gap-3 mt-15 md:mx-20 ">
    <div class="text-3xl font-bold">Popular Items</div>
    <div class="text-xl font-base">Popular items in this week</div>
  <div class="grid grid-cols-1 items-center justify-center sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-6 px-4 mt-2 mb-20">
    <ProductCard
      v-for="product in products"
      :key="product.id"
      :image="product.image"
      :name="product.name"
      :price="product.price"
    />
  </div>
  </div>
</template>

<script>
import ProductCard from '@/components/ProductCard.vue';

export default {
  components: {
    ProductCard
  },
  data() {
    return {
      products: [
        { id: 1, name: 'Orange Luxurious Bag', price: 160, image:'/public/luxurious-bag2.b6a7f2db4efe7c28a863.jpg'},
        { id: 2, name: 'Smart Watch', price: 200, image: '/public/smart-watch.66a34d60facdbb2a30f0.jpg' },
           { id: 3, name: 'White Sandals', price:120, image: '/public/fashion-shoes-sneaker.aab3c6439c42ef3bb22e.jpg' },
              { id: 4, name: 'Ladies Skirt', price: 550, image: '/public/ladies-skirt-pair.688f4be5bee4169b214f.jpg' }

      ]
    };
  }
};
</script>


