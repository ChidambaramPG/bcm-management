<template>
  <div id="">
    <top-bar />
    <div class="container">
      <categories-header/>
      <categories-list class="brochures-table" v-if="getCategorySection == 'table'"/>
      <add-new-category v-else-if="getCategorySection == 'new'"/> 
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import CategoriesList from "../components/categories/CategoriesList.vue";
import CategoriesHeader from "../components/categories/CategoriesHeader.vue";
import AddNewCategory from '../components/categories/AddNewcategory.vue';
import store from '../../store/index.js'
export default {
  name: "Categories",
  components: {
    TopBar,
    CategoriesHeader,
    CategoriesList,
    AddNewCategory
  },
  computed:{
    getCategorySection(){
      return store.state.categorySection;
    }
  }
};
</script>
<style scoped>
.brochures-table {
  margin-top: 20px;
}
</style>
