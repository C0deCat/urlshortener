<template>
<div class="mdl-layout mdl-js-layout mdl-layout--fixed-header mdl-layout--no-drawer-button">
  <Header></Header>
  <PageContent></PageContent>
</div>
</template>

<script>
import Header from "./components/headerTop.vue";
import PageContent from "./components/pageContent.vue";

export default {
  name: "App",
  components: {
    Header,
    PageContent
},
};
</script>

<style lang="less">
</style>
