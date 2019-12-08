<template>
  <button 
    class="list-group-item active-section"
    @click.prevent="() => setContentLayout(name)"
    v-if="activePage == name"
  >
    {{ convertName(name) }}
  </button>
  <button 
    class="list-group-item list-group-item-action"
    @click.prevent="() => setContentLayout(name)"
    v-else
  >
    {{ convertName(name) }}
  </button>
</template>
<script>
import store from '../../../store/index.js';
export default {
  name: "SidebarMenuItem",
  methods: {
    setContentLayout: page => {
      console.log("setting page", page);
      store.commit("setActivePage", page);
    },
    convertName(name){
      return name.charAt(0).toUpperCase()+name.slice(1)
    }
  },
  props: ["name"],
  computed:{
      activePage(){
          return store.state.activePage;
      }
  }
};
</script>
<style scoped>
.active-section {
  background-color: #f95473;
  color: white;
  text-align:right;
}
</style>
