<template>
  <div class="containerMn">
    <div class="reviewGroup">
      <div v-html="$md.render(reviewgroupdata.richText)" />

      <div class="reviewGroupItem">
        <a
          v-for="item in reviewgroupdata.images"
          :key="item.key"
          target="_blank"
          href="https://www.google.com/search?hl=en-US&gl=us&q=Great+Lakes+Entry+Systems,+87+Taylor+St,+Quincy,+MI+49082&ludocid=12307431422042846888&lsig=AB86z5VlE1Jv8Ji_9nqhZ6n94YBA&hl=en&gl=US#lrd=0x883d7ce14d53547d:0xaaccc7abb85836a8,1"
        >
          <img :src="item.image.url" alt="image">
        </a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    reviewgroupdata: {
      type: Object,
      required: true
    }
  }

}
</script>

<style>

</style>
