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
          <b-col cols="3"><h3>About</h3></b-col>
          <b-col cols="9"><p class="type-s" v-html="entry.introductionText"></p></b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><h3>Case study Zurich</h3></b-col>
          <b-col cols="9"><p class="type-s">{{entry.caseStudyText}}</p></b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="12" offset="0">
            <div style="padding:56.25% 0 0 0;position:relative;">
              <iframe src="https://player.vimeo.com/video/357958503?title=0&byline=0&portrait=0" style="position:absolute;top:0;left:0;width:100%;height:100%;" frameborder="0" allow="autoplay; fullscreen" allowfullscreen></iframe>
            </div>
          </b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><h3>Featured</h3></b-col>
          <b-col cols="9">
            <p class="type-s"><a class="inline-link" href="https://deepcity.ch/">Deep City</a>, 2020-21 International Latsis Symposium, EPFL, Lausanne, CH</p>
            <p class="type-s"><a class="inline-link" href="https://futurearchitectureplatform.org">Ideas 2020</a>, Future Architecture Platform, Ljubljana, SI</p>
            <p class="type-s"><a class="inline-link" href="https://projectarchitecture.com/city-as-verb">City as Verb</a>, Seoul New Hall of Architecture and Urbanism, Seoul, KO</p>
            <p class="type-s"><a class="inline-link" href="http://seoulbiennale.org/">Collective City</a>, The Seoul Biennale of Architecture and Urbanism 2019, Seoul, KO</p>
          </b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><h3>My City</h3></b-col>
          <b-col cols="9"><p class="type-s">I am interested in a collaborating on my city: <a class="inline-link" href="mailto:scott@ten.studio?subject=Lets%20make%20a%20Distributed%20Cooperative%20in%20[YOURCITY]">Get in contact.</a></p></b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><h3>Team</h3></b-col>
          <b-col cols="9">
            <p class="type-s s-b-8"><span>Scott Lloyd</span> is an architect based in Zurich. He is a founding member of TEN Studio where he works on architecture, research and urban transformation.</p>
            <p class="type-s s-b-8"><span>Alexis Kalagas</span>  is an urban strategist and writer based in Melbourne. His work focuses on innovation in urban development through emerging digital technologies.</p>
            <p class="type-s s-b-8"><span>Eva Candela</span> is an architect, and photographer. She is currently guest professor at Department of Architectural Projects, University of Alicante.</p>
            <p class="type-s s-b-8"><span>Max Frischknecht</span>  is a design researcher, programmer, and graphic designer. His works focuses on the impact of digitization on various areas of society. He is currently pursuing a Ph.D. in Digital Humanities at the University of Bern</p>
          </b-col>
        </b-row>
        <b-row class="content-block">
          <b-col cols="3"><h3>Credits</h3></b-col>
          <b-col cols="9">
            <p class="type-s subtitle">The Distributed Cooperative</p>
            <p class="type-s s-b-8">Scott Lloyd (TEN), Alexis Kalagas, Nemanja Zimonjic (TEN)</p>
            <p class="type-s subtitle">Film Production</p>
            <p class="type-s s-b-8">Adam Walker</p>
            <p class="type-s subtitle">Production contribution</p>
            <p class="type-s s-b-8">Tamim Hokanr</p>
            <p class="type-s subtitle">Programming</p>
            <p class="type-s s-b-8">Reinhard Koenig, Husain Vaghjipurwala, Martin Bielik</p>
            <p class="type-s subtitle">Seoul Biennale installation design</p>
            <p class="type-s s-b-8">Scott Lloyd, Alexis Kalagas, Nemanja Zimonjic</p>
            <p class="type-s subtitle">Design of depicted spaces</p>
            <p class="type-s s-b-8">Scott Lloyd, Nemanja Zimonjic, Jana Kulic, Milan Ivanovic, Ognjen Krasna, Alexis Kalagas</p>
            <p class="type-s subtitle">Model photography</p>
            <p class="type-s s-b-8">Milos Martinovic</p>
            <p class="type-s subtitle">Orignal architecture content</p>
            <p class="type-s s-b-8">Nicola Campri, Lucio Crignola, Milan Ivanovic, Jana Kulic, Chiara Malerba, Guillaume Othenin-Girard, Tobia Rapelli, Nico Rothenbuehler, Margherita Sorgentone, Francisco Moura Veiga</p>
            <p class="type-s subtitle">Web design and development</p>
            <p class="type-s s-b-8">Max Frischknecht</p>
            <p class="type-s subtitle">Support by</p>
            <p class="type-s s-b-8">City of Zurich, Pro Helvetia, DeCodingSpaces, TEN</p>
          </b-col>
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
          introductionText: 'Addressing the generational challenge of scaling non-speculative housing models, the Distributed Cooperative demonstrates how mixed-use cooperative housing can be reimagined at a neighbourhood scale.<br><br>Using customised scripting, the project is able to automatically identify under-utilised, well located building sites from open spatial data sets. These sites can be clustered within walkable distances, and each contribute a shared common space across a network of cooperative sites.<br><br>From communal kitchens, co-working spaces, to wellness rooms the project gives public access for the communal arrangement of urban space, and thereby offers new means to recreate the city in the image of its citizens.',
          caseStudyText: 'The results of the 2011 referendum on affordable housing in Zurich legislated that by 2050 one-third of Zurich’s rental housing must operate on a non-profit basis. Housing cooperatives already account for 70 percent of the non-profit rental stock, but a lack of affordable sites and the rapid growth of the market housing sector, make it increasingly unlikely that the public mandate will be reached by 2050. New models are clearly needed to address the current and future supply crisis for compact, legitimate and sustainable urban habitation. ',
        }
      }
    },
  }
</script>

<style lang="scss" scoped>
#overlay {
  padding: 1.2rem 0rem 0rem 0rem;
  width: 50%;
  height: 100vh;
  position: fixed;
  z-index: 100;
  top: 0;
  right: 0;
  background-color: white;
  overflow-y: scroll;
  background: #FFFFFF;
  box-shadow: 0 20px 20px 10px rgba(0, 0, 0, 0.2);
  // mix-blend-mode: exclusion;
}
#close-icon {
  position: fixed;
  top: 0.2rem;
  right: 1.8rem;
  cursor: pointer;
}
.content-block {
  padding-bottom: 3rem;
  & img {
    width: 100%;
  }
}
h3 {
  // letter-spacing: 0.2rem;
  // font-size: 1.5rem;
  // line-height: 1.8rem;
  // font-weight: 600;
}


.panelFade-enter-active, .panelFade-leave-active {
  transition: transform 1s;
}
.panelFade-enter, .panelFade-leave-to /* .fade-leave-active below version 2.1.8 */ {
  transform: translateX(100%);
}

</style>