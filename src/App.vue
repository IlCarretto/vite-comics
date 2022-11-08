<script>
import AppHeader from "./components/AppHeader.vue";
import OurContent from "./components/OurContent.vue";
import AppProducts from "./components/AppProducts.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    OurContent,
    AppProducts,
    AppFooter
  }
}
</script>

<template>
<AppHeader/>
<OurContent/>
<AppProducts/>
<AppFooter/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
