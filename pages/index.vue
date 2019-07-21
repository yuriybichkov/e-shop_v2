<template>
  <div>
    <HomeCarousel/>

    <b-container>
      <section class="mb-5">
        <h2 class="mb-3">Хиты сезона!</h2>
        <productsSlider :products="hitProducts"/>

      </section>

      <section class="mb-5">
        <h2 class="mb-3">Новинки</h2>
        <productsSlider :products="newProducts"/>
      </section>

    </b-container>
  </div>
</template>

<script>
  import HomeCarousel from "../components/HomeCarousel";
  import ProductsSlider from "../components/ProductsSlider";

  export default {
    components: {ProductsSlider, HomeCarousel},
    async asyncData({$axios}) {
      let hitProducts = [];
      let newProducts = [];
      try {
        hitProducts = await $axios.$get('/hit-slider.json');
        newProducts = await $axios.$get('/new_products-slider.json');
      } catch (e) {
        console.warn(e)
      }
      return {
        hitProducts,
        newProducts
      }
    },

  }

</script>

<style>

</style>
