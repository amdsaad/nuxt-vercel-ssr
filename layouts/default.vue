<template>
  <div>
    <navbar />
    <Nuxt />
    <app-footer />
    <footer>
      <div class="containerMn">
        <div class="copyright">
          Copyright &copy; 2014- {{ currentYear }}
          Great Lakes Entry | Website developed & hosted by
          <a href="https://schrader.co" target="blank"
            >Schrader Web Solutions</a
          >
        </div>
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear()
    };
  }
};
</script>
