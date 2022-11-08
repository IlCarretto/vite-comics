<script>
import AppHeader from "./components/AppHeader.vue";
import OurContent from "./components/OurContent.vue";
import AppProducts from "./components/AppProducts.vue";

export default {
  components: {
    AppHeader,
    OurContent,
    AppProducts,

  }
}
</script>

<template>
<AppHeader/>
<OurContent/>
<AppProducts/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
