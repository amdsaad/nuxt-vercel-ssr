<template>
  <div class="reviewGroupthree">
    <iframe
      :src="reviewgroupthreedata.map.url"
      :width="reviewgroupthreedata.map.width"
      :height="reviewgroupthreedata.map.height"
      style="border: 0"
      allowfullscreen=""
      loading="lazy"
    />
  </div>
</template>

<script>
export default {
  props: {
    reviewgroupthreedata: {
      type: Object,
      required: true
    }
  }

}
</script>

<style>

</style>
