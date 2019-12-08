<template>
  <div class="home">
    <div class="row" v-if="showSidebar">
      <div class="col-md-2 sidebar-content" >
        <sidebar/>
      </div>
      <div class="col-md-10 page-content border-left">
        <dashboard v-if="activePage==='dashboard'"/>
        <brochure v-else-if="activePage==='brochures'"/>
        <cards v-else-if="activePage==='cards'"/>
      </div>
    </div>
    <div class="row" v-else>
      <div class="col-md-12 page-content border-left">
        <dashboard v-if="activePage==='dashboard'"/>
        <brochure v-else-if="activePage==='brochures'"/>
        <cards v-else-if="activePage==='cards'"/>
      </div>
    </div>
    <div class="row">
      <all-modals/>
    </div>
    
        
  </div>
</template>

<script>
import Sidebar from "./shared/Sidebar.vue";
import Dashboard from './pages/Dashboard.vue';
import Brochure from './pages/Brochures.vue';
import Cards from './pages/Cards.vue';
import AllModals from './shared/AllModals.vue';
import store from '../store/index.js';

export default {
  name: "home",
  components: {
    Sidebar,
    Dashboard,
    Brochure,
    AllModals,
    Cards
  },
  computed:{
    showSidebar(){
      return store.state.sidebarVisible;
    },
    activePage(){
      return store.state.activePage;
    }
  }
};
</script>

<style scoped>

.page-content{
  padding: 0px;
}

.sidebar-content{
  padding:0px;
}

</style>
