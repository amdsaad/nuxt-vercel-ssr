<template>
  <div class="containerMn">
    <div class="doucksGroup">
      <div class="doucksGroupItem">
        <div class="doucksGroupItemBox">
          <h1>{{ doucksdataleft.title.title }}</h1>
          <ul>
            <li v-for="item in doucksdataleft.text" :key="item.id">
              <p>{{ item.text }}</p>
            </li>
          </ul>
        </div>
      </div>
      <div class="doucksGroupItem">
        <img :src="doucksdataright.image.image.url" alt="DSC_0463-scaled.jpg" class="DSC_0463-scaled">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    doucksdataleft: {
      type: Object,
      required: true
    },
    doucksdataright: {
      type: Object,
      required: true
    }
  }

}
</script>

<style>

</style>
