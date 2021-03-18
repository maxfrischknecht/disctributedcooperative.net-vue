<template>
  <div id="home">
    <Map></Map>
    <Overlay :overlay="overlay" :showHide="showHide"></Overlay>
    <div id="page-title" :class="{ moved : overlay }">
      <h1 @click="overlay = !overlay">The Distributed Cooperative</h1>
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

#page-title {
  transition: 0.4s;
  transform: translateY(48vh);
  width: 100%;
  height: 4.8rem;
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
  & h1 {
    margin-top: 0.4rem;
    cursor: pointer;
    // background-color: white;
    padding: 0.6rem 0.8rem;
    user-select: none;
  }
}
</style>
