<template>
  <div v-if="extrSectionsdata">
    <section
      v-for="(section, indx) in extrSectionsdata"
      :id="section.cssId"
      :key="indx"
    >
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
  props: {
    extrSectionsdata: {
      type: Array
    }
  }
};
</script>
