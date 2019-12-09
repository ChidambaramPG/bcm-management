<template>
  <div id="">
    <top-bar />
    <div class="container">
      <user-header />
      <user-list class="brochures-table" />
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import UserList from "../components/users/UserList.vue";
import UserHeader from "../components/users/UserHeader.vue";
export default {
  name: "Users",
  components: {
    TopBar,
    UserHeader,
    UserList
  }
};
</script>
<style scoped>
.brochures-table {
  margin-top: 20px;
}
</style>
