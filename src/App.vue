<template>
  <div id="app">
    <router-view id="content"></router-view>
  </div>
</template>

<script>

export default {
  name: 'app',
  metaInfo: () => ({
    link: [{ rel: "favicon", href: "favicon.ico" }],
    // if no subcomponents specify a metaInfo.title, this title will be used
    title: "The Distributed Cooperative",
    // all titles will be injected into this template
    description: "Addressing the generational challenge of scaling non-speculative housing models, the Distributed Cooperative demonstrates how customised scripting can help reimagine mixed-use cooperative housing at a neighbourhood scale. ",
  }),
}
</script>

<style lang="scss">
</style>
