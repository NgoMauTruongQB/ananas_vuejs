<template>
  <div id="app" class="container">
    <CompTopHeader> </CompTopHeader>
  </div>
</template>

<script>
import CompTopHeader from "./components/CompTopHeader.vue";
export default {
  name: "app",
  data() {
    return {};
  },
  components: {
    CompTopHeader,
  },
};
</script>

<style>
#app {
  margin: 0;
}
</style>
