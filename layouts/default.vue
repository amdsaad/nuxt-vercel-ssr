<template>
  <div>
    <navbar />
    <Nuxt />
    <app-footer />
    <footer>
      <div class="containerMn">
        <div class="copyright">
          Copyright &copy; 2014-
          <script>
            document.write(new Date().getFullYear());
          </script>
          Great Lakes Entry | Website developed & hosted by
          <a href="https://schrader.co" target="blank"
            >Schrader Web Solutions</a
          >
        </div>
      </div>
    </footer>
  </div>
</template>
