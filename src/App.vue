<template>
  <div class="container">
    <!-- <component :is="'appInital'" /> -->
    <component :is="screens[position]" />
  </div>
</template>

<script>
import appInital from "./components/intialCom.vue";
import appConfirm from "./components/confirmCom.vue";
import appResults from "./components/resultsCom.vue";

export default {
  components: {
    appInital,
    appConfirm,
    appResults,
  },
  data() {
    return {
      screens: ["appInital", "appConfirm", "appResults"],
      position: 0,
    };
  },
};
</script>

<style>
@import "./assets/style.css";
</style>
