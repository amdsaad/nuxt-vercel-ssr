<template>
  <div>
    <section id="aboutHeader" class="header">
      <h1>About Us</h1>
    </section>
    <section id="mainID">
      <p>
        Great Lakes Entry Systems provides help to the disabled by specializing
        in custom designed wheelchair ramps, stairs, steps and platforms. We
        offer permanent and temporary systems for both commercial and
        residential applications.
      </p>
      <br />
      <p>
        Great Lakes Entry Systems is based on the principles of quality,
        customer satisfaction, honesty, and integrity. It is our mission to not
        only determine what your needs are, but to do everything we can to meet
        or exceed those needs. Our team based approach allows us to continuously
        improve our services while working toward the goal of being known as the
        most professional, dependable, and efficient supplier in the industry.
      </p>
      <br />
      <p>
        With our two decades of design and manufacturing experience, combined
        with a 100,000 square foot manufacturing facility in Quincy, Michigan,
        Great Lakes Entry Systems has both the expertise to insure quality and
        the commitment to stand behind our products for generations to come.
      </p>
      <h2>Great Lakes Entry Systems</h2>
      <p>
        87 Taylor Street <br />
        Quincy, Michigan 49082
      </p>
      <br />
      <p>(517) 639 7402</p>
    </section>
    <extra-sections :extrSectionsdata="extrSections" />
  </div>
</template>

<script>
import axios from "axios";

export default {
  async asyncData() {
    const extrSections = await axios.get(
      "https://strapi-greatlakesentry.herokuapp.com/shared"
    );
    console.log(extrSections.data);

    return { extrSections: extrSections.data };
  }
};
</script>
