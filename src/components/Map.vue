<template>
  <div id="map-wrapper">
    <div id="map">
      <img ref="p1" src="DC_buildings_lots_blue.gif">
    </div>
  </div>
</template>

<script>
  import { gsap } from "gsap"
  import Draggable from "gsap/Draggable";
  gsap.registerPlugin(Draggable);

  export default {
    name: 'Map',
    mounted() {
      Draggable.create(this.$refs.p1);
    }
  }
</script>

<style lang="scss" scoped>
  #map-wrapper {
    position: fixed;
    top: 0;
    left: 0;
    height: 100vh;
    width: 100%;
    overflow: hidden;
    & #map {
      position: relative;
      & img {
        min-width: 6000px;
        height: auto;
        transform: translate(-2500px,-2200px);
      }
    }
  }


</style>