<script setup lang="ts">
import { Product } from '../types/product';
import ProductItem from './ProductItem.vue';

interface Props {
  products: Product[]
}
  
defineProps<Props>();
</script>

<template>
  <div class="products__list p-4">
    <ProductItem v-for="product in products" :key="product.id" :product="product" />
  </div>
</template>

<style scoped>
.products__list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  row-gap: 4rem;
  column-gap: 24px;
}
</style>