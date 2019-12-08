<template>
  <div id="">
    <top-bar />
    <div class="container">
      <overview/>
      <brochures class="brochure-table"/>
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import Overview from '../shared/Overview.vue';
import Brochures from '../components/dashboard/Brochures.vue';
export default {
  name: "Dashboard",
  components: {
    TopBar,
    Overview,
    Brochures
  }
};
</script>
<style scoped>
.brochure-table{
  margin-top:100px;
}
</style>
