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
    title: "DD Boilerplate Vue",
    // all titles will be injected into this template
    description: "A fresh and cool boilerplate to make 🚀 websites",
  }),
}
</script>

<style lang="scss">
</style>
