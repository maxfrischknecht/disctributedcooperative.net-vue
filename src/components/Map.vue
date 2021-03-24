<template>
  <div id="map-wrapper">
    <div id="map">
      <img ref="p1" src="dc_zurich_map_5500.gif">
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
      const map = this.$refs.p1;
      Draggable.create(map);

      const script = (p5) => {

        let location = new p5.createVector(-3000, 3000);
        let noff = new p5.createVector(p5.random(-3000, 3000),p5.random(-3000, 3000));
        
        // setInterval(() => { 
        //   location.x = p5.map(p5.noise(noff.x),0,1,0,-3000, 3000);
        //   location.y = p5.map(p5.noise(noff.y),0,1,0,-3000, 3000);
          
        //   noff.add(0.1,0.1,0);
        //   console.log(location.x, location.y)

        //   map.style.transform = "translate(" + location.x + "px ,"  + location.y + "px)";
        // }, 3000)
        // NOTE: Draw is here
        p5.draw = () => {
          // let x_noise = p5.noise(100) * 100;
          // console.log(x_noise)

          location.x = p5.map(p5.noise(noff.x),0,1,0,-3000, 3000);
          location.y = p5.map(p5.noise(noff.y),0,1,0,-3000, 3000);
          
          noff.add(0.002 ,0.002 ,0);
          // console.log(location.x, location.y)

          map.style.transform = "translate(" + location.x + "px ,"  + location.y + "px)";
        }
      }
      const P5 = require('p5');
      new P5(script)
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
      transition: 0.3s;
      & img {
        min-width: 5500px;
        transition: 0.3s;
        height: auto;
        transform: translate(-2100px,-2100px);
      }
    }
  }


</style>