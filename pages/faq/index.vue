<template>
  <div>
    <section id="faqHeader" class="header">
      <h1>FAQ</h1>
    </section>
    <section id="mainID" class="faq">
      <h2>Vertical Lifts</h2>
      <h3>Why doesn’t my lift stay up?</h3>
      <p>
        If the winch doesn’t click going up, the winch is wound backwards.
        Clockwise: to wind up. Counter-Clockwise: to wind down. The winch needs
        a load to activate the brake. An empty lift may not stay up.
      </p>
      <br />
      <h3>Can I put the winch on either side of my lift?</h3>
      <p>
        No. But if you want to move the lift from one side of your dock to the
        other, simply turn your lift 180° at the same time. It doesn’t matter
        which end of the lift you drive onto.
      </p>
      <br />
      <h3>Will this lift work in shallow water?</h3>
      <p>
        This lift will operate in 9 inches of water, pluss the hull draft of
        your boat.
      </p>
      <br />
      <h3>Why do the rear cables of the lift appear slack? Is this okay?</h3>
      <p>
        The rear cables are only used to keep the cradle level. These cables
        only go into tension when the load weight of the watercraft is not
        centered. Then, only the cable on the heavy side is working and will
        appear tight. The cable on the light side is doing no work, so remains
        loose. If you tighten these cables they will bind and make the lift hard
        to crank.
      </p>
      <div class="white-line"></div>
      <h2>Jet Lifts</h2>
      <h3>Why doesn’t my lift stay up?</h3>
      <p>
        If the winch doesn’t click going up, the winch is wound backwards.
        Clockwise: to wind up. Counter-Clockwise: to wind down. The winch needs
        a load to activate the brake. An empty lift may not stay up.
      </p>
      <br />
      <h3>Can the winch be mounted on either side of the lift?</h3>
      <p>
        On a cantilever, yes. On a vertical you can rotate the lift 180%deg;. It
        doesn’t matter which end you enter the lift.
      </p>
      <br />
      <h3>Why does my jet lift crank down hard?</h3>
      <p>
        Winch shaft & wheel need grease. Wheel needs to thread on and off the
        shaft to activate and release the brake.
      </p>
      <br />
      <h3>How much weight does my lift hold?</h3>
      <p>
        All of our Jet Lifts hold a 1500lb capacity. Double Jet Lift is 3500lb
        capacity.
      </p>
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
