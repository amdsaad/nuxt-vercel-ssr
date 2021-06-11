<template>
  <div class="containerMn">
    <h1>{{ testimonialdata.section_title }}</h1>
    <VueSlickCarousel :arrows="true" :dots="false" v-bind="settings">
      <div
        v-for="(item, indx) in testimonialdata.testimonial_item"
        :key="indx"
        class="testimonialGroupitem"
      >
        <img :src="item.image.url" alt="t_img" />
        <div class="starItem">
          <ul class="starItemUL">
            <li><i class="fas fa-star" /></li>
            <li><i class="fas fa-star" /></li>
            <li><i class="fas fa-star" /></li>
            <li><i class="fas fa-star" /></li>
            <li><i class="fas fa-star" /></li>
          </ul>
        </div>
        <div class="testimonialGroupitemDes">
          <p><i class="fas fa-quote-left" />{{ item.text }}</p>
          <h6>{{ item.by }}</h6>
        </div>
      </div>
      <template #prevArrow>
        <div class="custom-arrow custom-arrow-left">
          <i class="fas fa-arrow-circle-left"></i>
        </div>
      </template>
      <template #nextArrow>
        <div class="custom-arrow custom-arrow-right">
          <i class="fas fa-arrow-circle-right"></i>
        </div>
      </template>
    </VueSlickCarousel>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";

export default {
  components: { VueSlickCarousel },

  props: {
    testimonialdata: {
      type: Object,
      required: true
    }
  },
  data() {
    return {
      settings: {
        arrows: true,
        dots: false,
        infinite: true,
        slidesToShow: 1,
        slidesToScroll: 1,
        autoplay: true,
        cssEase: "linear"
      }
    };
  }
};
</script>

<style>
@import "vue-slick-carousel/dist/vue-slick-carousel.css";
@import url("vue-slick-carousel/dist/vue-slick-carousel-theme.css");
</style>
