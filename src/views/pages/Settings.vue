<template>
  <div id="">
    <top-bar />
    <div class="container">
        <profile-settings/>
    </div>
  </div>
</template>

<script>
import TopBar from "../shared/TopBar.vue";
import ProfileSettings from '../components/profile/ProfileSettings.vue';
export default {
  name: "Settings",
  components: {
    TopBar,
    ProfileSettings
  }
};
</script>

<style></style>
