<template>
  <b-carousel
    class="mb-3"
    id="carousel-fade"
    style="text-shadow: 0px 0px 2px #000"

    fade
    indicators
    img-width="1024"
    img-height="440"
  >
    <b-container>

    <b-carousel-slide
      img-src="../static/Image_carousel/IMG_20170907_105528_HDR.jpg"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/IMG_20171005_095313.jpg"
    ></b-carousel-slide>

     <b-carousel-slide
      img-src="../static/Image_carousel/IMG_20171201_191203_HDR.jpg"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/IMG_20180724_111911.jpg"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/P7167712.JPG"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/P7167728.JPG"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/P7167734.JPG"
    ></b-carousel-slide>

    <b-carousel-slide
      img-src="../static/Image_carousel/P7167736.JPG"
    ></b-carousel-slide>

    </b-container>
  </b-carousel>


</template>

<script>
    export default {
      data() {
        return {
          slide: 0,
          sliding: null
        }
      },
      methods: {
        onSlideStart(slide) {
          this.sliding = true
        },
        onSlideEnd(slide) {
          this.sliding = false
        }
      }
    }
</script>

<style scoped>

</style>
