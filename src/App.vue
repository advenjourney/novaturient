<template>
  <div class="w-page">
    <v-header />
    <main class="main-content">
      <router-view />
    </main>
    <v-footer />
  </div>
</template>
<script>
import VHeader from "./components/VHeader.vue";
import VFooter from "./components/VFooter.vue";

export default {
  components: {
    VHeader,
    VFooter
  }
};
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
