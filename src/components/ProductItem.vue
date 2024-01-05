<script setup lang="ts">
import { Product } from '../types/product';

interface Props {
  product: Product
}

defineProps<Props>();
</script>

<template>
  <router-link :to="{ name: 'Product', params: { id: product.id } }">
    <article class="flex flex-col cursor-pointer hover:-translate-y-1 transition duration-300">
      <img :src="product.image" :alt="product.name" class="w-full h-full aspect-square object-cover" />
      <h1 class="font-bold text-lg mt-2">{{ product.name }}</h1>
      <p class="text-gray-400">{{ product.type }}</p>
      <p class="text-lg font-medium mt-2">${{ product.price }}</p>
    </article>
  </router-link>
</template>