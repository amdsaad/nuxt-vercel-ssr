<template>
  <VueSlickCarousel :arrows="true" :dots="true" v-bind="settings">
    <div v-for="(item,indx) in sliderdata " :key="indx" class="banner_group">
      <div class="banner_item">
        <img :src="item.image.url" alt="img">
        <div class="banner_itemBox">
          <h1>{{ item.title }}</h1>
          <p>
            {{ item.text }}
          </p>
          <nuxt-link id="bannerLmore" :to="item.url">
            Learn More <i id="LMoreIcom" class="fas fa-angle-right" />
          </nuxt-link>
        </div>
      </div>
    </div>
  </VueSlickCarousel>
</template>

<script>
import VueSlickCarousel from 'vue-slick-carousel'

export default {
  components: { VueSlickCarousel },
  props: {
    sliderdata: {
      type: Array,
      required: true
    }
  },
  data () {
    return {
      settings: {
        arrows: true,
        dots: true,
        infinite: true,
        slidesToShow: 1,
        slidesToScroll: 1,
        autoplay: true,
        cssEase: 'linear'
      }
    }
  },
  mounted () {
  }
}
</script>

<style>

@import url('vue-slick-carousel/dist/vue-slick-carousel.css');
@import url('vue-slick-carousel/dist/vue-slick-carousel-theme.css');
</style>
