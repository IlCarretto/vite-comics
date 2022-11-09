<script>
import AppHeader from "./components/AppHeader.vue";
import SeriesSection from "./components/SeriesSection.vue";
import AppProducts from "./components/AppProducts.vue";
import AppFooter from "./components/AppFooter.vue";

export default {
  components: {
    AppHeader,
    SeriesSection,
    AppProducts,
    AppFooter
  }
}
</script>

<template>
<AppHeader/>
<SeriesSection/>
<AppProducts/>
<AppFooter/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
