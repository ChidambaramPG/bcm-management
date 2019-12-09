<template>
  <div id="">
    <top-bar />
    <div class="container">
      <categories-header/>
      <categories-list class="brochures-table" />
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import CategoriesList from "../components/categories/CategoriesList.vue";
import CategoriesHeader from "../components/categories/CategoriesHeader.vue";
export default {
  name: "Categories",
  components: {
    TopBar,
    CategoriesHeader,
    CategoriesList
  }
};
</script>
<style scoped>
.brochures-table {
  margin-top: 20px;
}
</style>
