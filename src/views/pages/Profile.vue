<template>
  <div id="">
    <top-bar />
    <div class="container">
        <profile-details/>
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import ProfileDetails from '../components/profile/ProfileDetails.vue';
export default {
  name: "Profile",
  components: {
    TopBar,
    ProfileDetails
  }
};
</script>

<style></style>
