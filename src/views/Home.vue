<script setup lang="ts">
import ProductList from "../components/ProductList.vue";
import { productsMock } from "../__mock/products";
import Banner from "../components/Banner.vue";

</script>

<template>
  <main class="flex flex-col items-center gap-12">
    <Banner src="https://nikevideo.nike.com/media/v1/pmp4/static/clear/72451143001/d0b18cc2-12dc-4a25-a04f-91c07232c5ae/4d2cb845-e012-4249-85dd-6ac4372d8849/main.mp4"/>
    <section class="container">
      <ProductList :products="productsMock"/>
    </section>
  </main>
</template>