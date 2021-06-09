<template>
  <section v-if="footerData" :id="footerData.cssID">
    <div class="containerMn">
      <div class="footerGroup">
        <div class="footerGroupitem">
          <nuxt-link :to="footerData.first_col.image.url">
            <img
              :src="footerData.first_col.image.image.url"
              alt="fotterlogo"
              class="footerLogo"
            />
          </nuxt-link>

          <ul
            v-for="(link, indx) in footerData.first_col.textwithicon"
            :key="indx"
            class="socialMidea"
          >
            <li><i :class="link.icon"></i></li>
            <li>{{ link.text }}</li>
          </ul>
        </div>
        <div class="footerGroupitem">
          <p><b>Quick Links</b></p>
          <ul class="linkUL">
            <li v-for="link in footerData.second_col.link" :key="link.id">
              <i class="fas fa-angle-double-right"></i>
              <nuxt-link :to="link.url">{{ link.text }}</nuxt-link>
            </li>
          </ul>
        </div>
        <div class="footerGroupitem">
          <p><b> Products </b></p>
          <ul class="linkUL">
            <li v-for="link in footerData.third_col.link" :key="link.id">
              <i class="fas fa-angle-double-right"></i>
              <nuxt-link :to="link.url">{{ link.text }}</nuxt-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      footerData: null,
    }
  },
  async fetch() {
    try {
      const data = await this.$strapi.find('footer')
      this.footerData = data
    } catch (error) {
      if (error.response.status == 404) {
        this.footerData = null
      }
    }
  },
}
</script>

<style></style>
