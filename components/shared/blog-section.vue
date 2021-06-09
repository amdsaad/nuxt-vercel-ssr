<template>
  <div>
    <div class="blog-title">
      <h1>Latest News & Updates</h1>
    </div>
    <div
      v-for="(item, indx) in blogdata"
      :key="indx"
      class="blog-section"
      id="blogsection"
    >
      <div class="blog-container">
        <div class="blog-container__text">
          <h1>{{ item.title }}</h1>
          <p>{{ item.text }}</p>
        </div>
        <div class="blog-container__img">
          <img :src="item.image.url" alt="bog image" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    blogdata: {
      type: Array,
      required: true,
    },
  },
}
</script>
