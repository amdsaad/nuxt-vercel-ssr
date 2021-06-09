<template>
  <div class="containerMn">
    <h1>{{ servicesdata.title }}</h1>
    <div class="serviceGRoup">
      <div v-for="(item,indx) in servicesdata.service_item" :key="indx" class="serviceGRoupitem">
        <div class="aserviceImg">
          <img :src="item.image.url" alt="service img">
          <a href="/products/stationary-docks">
            <h2>{{ item.title }}</h2>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    servicesdata: {
      type: Object,
      required: true
    }
  }

}
</script>

<style>

</style>
