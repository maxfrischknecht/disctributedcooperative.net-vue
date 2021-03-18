<template>
  <div id="home">
    <Map></Map>
    <!-- <b-container>
      <b-row>
        <b-col cols="12" offset="6">
          <h1>Hello World</h1>
        </b-col>
      </b-row>
    </b-container> -->
  </div>
</template>

<script>
import Map from "@/components/Map";

export default {
  name: 'app',
  metaInfo: () => ({
    link: [{ rel: "favicon", href: "favicon.ico" }],
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "The Distributed Cooperative",
    // all titles will be injected into this template
    description: "The Distributed Cooperative",
  }),
  components: {
    Map,
    
  },
  data() {
    return {
      document: [],
    };
  },

}
</script>

<style lang="scss">
@import "../assets/css/master.scss";

</style>
