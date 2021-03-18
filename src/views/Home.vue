<template>
  <div id="home">
    <b-container>
      <b-row>
        <b-col cols="12" offset="6">
          <h1>Hello World</h1>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
// import Header from "@/components/_shared/_header";

export default {
  name: 'app',
  metaInfo: () => ({
    link: [{ rel: "favicon", href: "favicon.ico" }],
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "DD Boilerplate Vue",
    // all titles will be injected into this template
    description: "A fresh and cool boilerplate to make 🚀 websites",
  }),
  components: {
    // Header,
    
  },
  data() {
    return {
      document: [],
    };
  },
  created () {
     let credits = `
        __               __                     __
       |  |      ___    |  |                   |  | 
       |  |     /__/    |  |                   |  |   ___
 ______|  |  _________  |  | ____   ___    ___ |  |__/__/
/  /   |  | /   /  |  | |   / |  | /  /   |  | |  |
|  |   |  | |  |___|__/ |  |  |  | |  |   |  | |  |
|  |   |  | |  |    ___ |  |  |  | |  |   |  | |  |   ___
|__|__/__/| |__|___/__/ |__|__/__/ |__|__/__/| |__|__/__/
        __               __                     __
       |  |      ___    |  |                   |  | 
       |  |     /__/    |  |                   |  |   ___
 ______|  |  _________  |  | ____   ___    ___ |  |__/__/
/  /   |  | /   /  |  | |   / |  | /  /   |  | |  |
|  |   |  | |  |___|__/ |  |  |  | |  |   |  | |  |
|  |   |  | |  |    ___ |  |  |  | |  |   |  | |  |   ___
|__|__/__/| |__|___/__/ |__|__/__/ |__|__/__/| |__|__/__/

Hello fellow digital nativ!  
This site was made by Début Début (Alain Brusch, Max Frischknecht, Philipp Möckli & Adrian Schnegg) in 2021
https://debutdebut.com
`;

    console.log(credits);
  },
 

}
</script>

<style lang="scss">
@import "../assets/css/master.scss";

</style>
