<script setup lang="ts">
import { ShoppingCart } from 'lucide-vue-next';

</script>

<template>
  <nav class="px-6 py-4 border-b flex flex-row items-center justify-between">
    <div class="flex items-center gap-4">
      <router-link to="/"><img src="https://static.nike.com.br/v10-306-1/images/brands/logo.svg" alt="Logo nike"></router-link>
    </div>
    <router-link to="/cart">
      <button class="bg-black px-4 py-1 text-white rounded-lg hover:bg-gray-700 transition duration-300 flex items-center gap-2">
        <ShoppingCart class="w-4"/>
        Cart
      </button>
    </router-link>
  </nav>
</template>