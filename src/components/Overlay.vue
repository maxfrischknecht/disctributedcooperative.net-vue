<template>
  <transition name="panelFade">
    <div id="overlay" v-if="overlay">
      <!-- <div @click="showHide()" id="close-icon">
        <svg width="19px" height="19px" viewBox="0 0 19 19" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
          <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
              <g transform="translate(-989.000000, -14.000000)" fill="#000000">
                  <g transform="translate(987.000000, 12.000000)">
                      <rect transform="translate(11.500000, 12.000000) rotate(-315.000000) translate(-11.500000, -12.000000) " x="0" y="11" width="23" height="2"></rect>
                      <rect transform="translate(12.000000, 11.500000) rotate(-315.000000) translate(-12.000000, -11.500000) " x="11" y="0" width="2" height="23"></rect>
                  </g>
              </g>
          </g>
        </svg>
      </div> -->
      <b-container fluid>
        <b-row class="content-block">
          <b-col cols="3"><p>About</p></b-col>
          <b-col cols="9"><p class="type-s">{{entry.text}}</p></b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="9" offset="1">
            <img src="https://ten.studio/images/curatingMaterial/Distributed_cooperative.png" alt="The Distributed Cooperative">
          </b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><p>Team</p></b-col>
          <b-col cols="9"><p class="type-s" v-html="entry.team"></p></b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><p>Contact</p></b-col>
          <b-col cols="9"><p class="type-s" v-html="entry.contact"></p></b-col>
        </b-row>
      </b-container>
    </div>
  </transition>
</template>

<script>
  export default {
    name: "Overlay",
    props: {
      overlay: {
        type: Boolean,
        required: true,
      },
      showHide: {
        type: Function,
        required: true
      }
    
    },
    data() {
      return {
        entry: {
          text: 'Addressing the generational challenge of scaling non-speculative housing models, the Distributed Cooperative demonstrates how customised scripting can help reimagine mixed-use cooperative housing at a neighbourhood scale. The results of the 2011 referendum on affordable housing in Zurich legislated that by 2050 one-third of Zurich’s rental housing must operate on a non-profit basis. Housing cooperatives already account for 70 percent of the non-profit rental stock, but a lack of affordable sites and the rapid growth of the market housing sector, make it increasingly unlikely that the public mandate will be reached by 2050. This calls for new models to address the current and future supply crisis for well located, compact, and socially legitimate urban habitation. The project responds by developing customised scripts that have automatically identify over 3500 under-utilised, well located potential building sites from open spatial data sets. Using parametric programming, the project is able to generate clusters of mixed-use buildings, each contributing a shared common space across a network of sites within walkable distances. From communal kitchens, co-working spaces, to wellness rooms the project gives public access for the communal arrangement of urban space, and thereby offers new means to recreate the city in the image of its citizens. ',
          team: 'Scott Lloyd <br>Alexis Kalagas <br>Nemanja Zimonjic<br>Eva Candela Castaño<br>Max Frischknecht',
          contact: 'www.ten.studio<br>scott@ten.studio'
        }
      }
    },
  }
</script>

<style lang="scss" scoped>
#overlay {
  padding: 0.8rem 0rem;
  width: 50%;
  height: 100vh;
  position: fixed;
  z-index: 100;
  top: 0;
  right: 0;
  background-color: white;
  overflow-y: scroll;
}
#close-icon {
  position: fixed;
  top: 0.2rem;
  right: 1.8rem;
  cursor: pointer;
}
.content-block {
  padding-bottom: 1.6rem;
  & img {
    width: 100%;
  }
}

.panelFade-enter-active, .panelFade-leave-active {
  transition: transform 1s;
}
.panelFade-enter, .panelFade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  transform: translateX(100%);
}

</style>