<template>
  <div id="">
    <top-bar />
    <div class="container">
      <brochure-header />
      <brochures class="brochures-table" />
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import Brochures from "../components/dashboard/Brochures.vue";
import BrochureHeader from "../components/bochures/BrochureHeader.vue";
export default {
  name: "Brochure",
  components: {
    TopBar,
    BrochureHeader,
    Brochures
  }
};
</script>
<style scoped>
.brochures-table {
  margin-top: 20px;
}
</style>
