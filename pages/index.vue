<template>
  <div class="homepage" v-if="homepage">
    <section
      v-for="(section, indx) in homepage.section"
      :id="section.cssId"
      :key="indx"
    >
      <slider
        v-if="section.Slick_slide_item"
        :sliderdata="section.Slick_slide_item"
      />
      <services
        v-if="section.__component == 'groups.service-group'"
        :servicesdata="section"
      />
      <doucks
        v-if="section.__component == 'groups.doucks-group'"
        :doucksdataleft="section.doucksleft"
        :doucksdataright="section.doucksright"
      />
      <testimonial
        v-if="section.__component == 'groups.testimonial-group'"
        :testimonialdata="section"
      />
      <reviewGroup
        v-if="section.__component == 'groups.review-group'"
        :reviewgroupdata="section"
      />
      <reviewGrouptwo
        v-if="section.__component == 'groups.review-group-two'"
        :reviewgrouptwodata="section"
      />
      <reviewGroupThree
        v-if="section.__component == 'groups.review-group-three'"
        :reviewgroupthreedata="section"
      />
      <blog-section
        v-if="section.__component == 'groups.blog'"
        :blogdata="section.blog_item"
      />
    </section>
  </div>
</template>

<script>
export default {
  async asyncData({ $strapi }) {
    const homepage = await $strapi.find('homepage')
    console.log(homepage)
    return { homepage }
  },
}
</script>
