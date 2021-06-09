<template>
  <div class="containerMn">
    <div class="reviewGrouptwo">
      <h2>
        <i>{{ reviewgrouptwodata.title1 }}</i>
      </h2>
      <h2><i>{{ reviewgrouptwodata.title2 }}</i></h2>
      <a v-for="item in reviewgrouptwodata.images " :key="item.id" :href="item.url">
        <img :src="item.image.url" :alt="item.image.url">
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    reviewgrouptwodata: {
      type: Object,
      required: true
    }
  }

}
</script>

<style>

</style>
