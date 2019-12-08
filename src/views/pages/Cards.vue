<template>
  <div id="">
    <top-bar />
    <div class="container">
      <cards-header />
      <business-cards class="brochures-table" />
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import BusinessCards from "../components/cards/BusinessCards.vue";
import CardsHeader from "../components/cards/CardsHeader.vue";
export default {
  name: "Cards",
  components: {
    TopBar,
    CardsHeader,
    BusinessCards
  }
};
</script>
<style scoped>
.brochures-table {
  margin-top: 20px;
}
</style>
