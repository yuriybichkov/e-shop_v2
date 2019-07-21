<template>
  <no-ssr>
    <carousel
      :margin="10" :items="5" :nav="false" :autoplay="true" :autoplayHoverPause="true" :dots="false"
      class="relative">
      <template slot="prev"><span class="prev"></span></template>
      <template slot="next"><span class="next"></span></template>
      <div v-for="product of products" :key="product.id">
        <div>
          <b-img class="mb-3" :src="product.image" fluid :alt="product.name"/>
          <h5 class="mb-2">{{product.name}}</h5>
          <div class="d-flex justify-content-between align-items-center">
            <strong>{{product.price}} ₴</strong>
            <b-button variant="warning">Купить</b-button>
          </div>
        </div>
      </div>
    </carousel>
  </no-ssr>
</template>

<script>
  export default {
    name: "ProductsSlider",
    props: {
      products: {
        type: Array,
        required: true
      }
    },
  }
</script>

<style scoped>
  .relative {
    position: relative;
  }

  .prev, .next {
    position: absolute;
    top: calc(50% - 60px);
    cursor: pointer;
  }

  .prev::before, .next::before {
    font-size: 40px;
    color: #343a40;
  }

  .prev {
    left: -50px;
  }

  .prev::before {
    content: '◄';
  }

  .next {
    right: -50px;
  }

  .next::before {
    content: '►';
  }

</style>

