<template>
  <div>
    <Head>
      <Title>Nuxt Dojo | {{ product.title }}</Title>
      <Meta name="description" :content="product.description" />
    </Head>
    <ProductDetails :product="product"/>
  </div>
</template>

<script setup lang="ts">

const { id } = useRoute().params;

const uri = `http://fakestoreapi.com/products/${id}`;

const { data: product } = await useFetch(uri, { key: String(id) });

if(!product.value) {
  throw createError({statusCode:404, statusMessage:'Product Not Found',fatal:true})
}

definePageMeta({
  layout: "products-single",
});
</script>

<style scoped></style>
