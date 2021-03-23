<template>
  <div id="home">
    <div id="ten-logo" :class="{ moved : overlay }">
      <h1><a href="https://ten.studio" target="_blank">X = ( T = E = N )</a></h1>
    </div>
    <Map></Map>
    <Overlay :overlay="overlay" :showHide="showHide"></Overlay>

    <div id="page-title" :class="{ moved : overlay }">
      <div>
        <h2 class="spacing-hover" @click="overlay = !overlay">
          The Distributed Cooperative <br>
          <span>Prototype One Zürich</span>
        </h2>
        <!-- <p>Prototype One: Zürich</p> -->
      </div>
    </div>
  </div>
</template>

<script>
import Map from "@/components/Map";
import Overlay from "@/components/Overlay";

export default {
  name: 'app',
    metaInfo: () => ({
    link: [{ rel: "favicon", href: "favicon.ico" }],
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "The Distributed Cooperative",
    // all titles will be injected into this template
    description: "Addressing the generational challenge of scaling non-speculative housing models, the Distributed Cooperative demonstrates how customised scripting can help reimagine mixed-use cooperative housing at a neighbourhood scale. ",
  }),
  components: {
    Map,
    Overlay
  },
  data() {
    return {
      document: [],
      overlay: false
    };
  },
  methods: {
    showHide() {
      this.overlay = !this.overlay;
    }
  }

}
</script>

<style lang="scss">
@import "../assets/css/master.scss";

#ten-logo {
  width: 100%;
  display: flex;
  justify-content: center;
  top: 0.8rem;
  height: 4.8rem;
  position: fixed;
  z-index: 90;
  transition: 1s;
  &.moved {
    width: 50%;
    transition: 1s
  }
}

#page-title {
  transition: 0.4s;
  transform: translateY(48vh);
  width: 100%;
  // margin: auto;
  position: fixed;
  z-index: 90;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: 1s;
  &.moved {
    width: 50%;
    transition: 1s
  }
  & h2 {
    cursor: pointer;
    text-align: center;
    background-color: transparent;
    box-shadow: none;
    letter-spacing: 0.8rem;
    text-transform: uppercase;
    padding: 0 !important;
    margin: 0 !important;
    transition: 0.5s;
    display: block;
    user-select: none;
    &:hover {
      // color:$color-primary;
      // text-decoration: underline;
      transition: 0.5s;
    }
    & span {
      // letter-spacing: 0.1rem;
      // font-size: 2rem;
      text-transform: none;
    }
  }
}
</style>
