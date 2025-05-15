<template>
  <div class="w-full bg-gray-900 text-white py-10 lg:mr-0">
    <div class="px-4 flex flex-col md:flex-row md:justify-between gap-10 max-w-screen-xl mx-auto">
      
    
      <div class="flex-1">
        <img src="/public/download.png" alt="">
        <p class="text-sm text-gray-400 max-w-xs">Discover the best products and deals every day.</p>
      </div>

      <div class="flex-1">
        <h3 class="text-xl font-semibold mb-3">Quick Links</h3>
        <ul class="space-y-2 text-sm text-gray-300">
          <li><a href="/" class="hover:underline">Home</a></li>
          <li><a href="/shop" class="hover:underline">Shop</a></li>
          <li><a href="/cart" class="hover:underline">Cart</a></li>
          <li><a href="/contact" class="hover:underline">Contact Us</a></li>
        </ul>
      </div>

  
      <div class="flex-1">
        <h3 class="text-xl font-semibold mb-3">Subscribe to our newsletter</h3>
        <form class="flex flex-col sm:flex-row sm:items-center sm:space-x-2">
          <input
            type="email"
            placeholder="Email address"
            class="flex-1 p-2 rounded text-black mb-2 sm:mb-0 bg-gray-100"
          />
          <button
            type="submit"
            class="bg-primary text-white py-2 px-4 rounded w-full sm:w-auto"
          >
            Subscribe
          </button>
        </form>
      </div>

    </div>

    <div class="text-center text-sm text-gray-500 mt-8">
      © 2025 MyShop. All rights reserved.
    </div>
  </div>
</template>


