<template>
  <section id="headerID">
    <div class="nav">
      <div class="navGroup">
        <div class="navGroupitem nav1">
          <nuxt-link to="/">
            <img src="/images/1logo2.png" alt="logo" class="navlogo" />
          </nuxt-link>
        </div>
        <div class="navGroupitem nav2">
          <ul class="manuUL">
            <li>
              <nuxt-link to="/about-us"> About Us </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/dealers"> Dealers </nuxt-link>
            </li>
            <li>
              <nuxt-link to="/faq"> FAQ </nuxt-link>
            </li>
            <li>
              <nuxt-link to="#"> Products </nuxt-link>
              <ul class="submanu">
                <li>
                  <nuxt-link to="#"> Starr Docks </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Accessories </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Canopies </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Dock Supports </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Platinum Dock </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Floating Docks </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Roll-in Docks </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr Lifts </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Starr PWC / Jet Ski Lifts </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Aluminum Stairs </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> SledShed Trailers </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Purchase or Rent? </nuxt-link>
                </li>
                <li>
                  <nuxt-link to="#"> Owners Info </nuxt-link>
                </li>
              </ul>
            </li>
            <li>
              <nuxt-link to="/contact-us"> Contact Us </nuxt-link>
            </li>
          </ul>
        </div>
        <div class="navGroupitem nav3">
          <div class="nav3Box">
            <ul class="nav3BoxUL">
              <li>
                <span id="Barger" @click="shownav3Links = !shownav3Links">
                  <i class="fas fa-bars" />
                </span>
                <ul v-if="shownav3Links" class="manuULMovile">
                  <li>
                    <nuxt-link to="#"> Home </nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#"> About Us </nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#"> Dealers </nuxt-link>
                  </li>
                  <li>
                    <nuxt-link to="#"> FAQ </nuxt-link>
                  </li>
                  <li>
                    <button
                      id="ProductsmanuId"
                      @click="showProductsmanuId = !showProductsmanuId"
                    >
                      Products <i class="fas fa-angle-down" />
                    </button>
                    <ul
                      v-if="showProductsmanuId"
                      id="submanuMObile"
                      class="submanuMObile"
                    >
                      <li>
                        <nuxt-link to="#"> Starr Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Accessories </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Canopies </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Dock Supports </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Platinum Dock </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Floating Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Roll-in Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Lifts </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#">
                          Starr PWC / Jet Ski Lifts
                        </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Aluminum Stairs </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> SledShed Trailers </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Purchase or Rent? </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Owners Info </nuxt-link>
                      </li>
                    </ul>
                  </li>
                  <li>
                    <button
                      id="ServicesId"
                      @click="showServicesMObile = !showServicesMObile"
                    >
                      Services <i class="fas fa-angle-down" />
                    </button>
                    <ul
                      v-if="showServicesMObile"
                      id="ServicesMObile"
                      class="submanuMObile"
                    >
                      <li>
                        <nuxt-link to="#"> Starr Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Accessories </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Canopies </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Dock Supports </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Platinum Dock </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Floating Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Roll-in Docks </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Starr Lifts </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#">
                          Starr PWC / Jet Ski Lifts
                        </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Aluminum Stairs </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> SledShed Trailers </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Purchase or Rent? </nuxt-link>
                      </li>
                      <li>
                        <nuxt-link to="#"> Owners Info </nuxt-link>
                      </li>
                    </ul>
                  </li>
                  <li>
                    <nuxt-link to="#"> Contact Us </nuxt-link>
                  </li>
                </ul>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      shownav3Links: false,
      showProductsmanuId: false,
      showServicesMObile: false
    };
  }
};
</script>

<style></style>
