<script>
import Navbar from "@/components/Navbar/Navbar.vue";
export default {
  name: "App",
  components: { Navbar },
  data() {
    return {
      content: "",
    };
  },
  computed: {
    mobile() {
      if (window.innerHeight <= 768) {
        return true;
      } else {
        return false;
      }
    },
  },
  watch: {
    $route(to) {},
  },
};
</script>

<template>
  <Navbar v-if="!mobile" />
  <div id="main">
    <RouterView />
  </div>
</template>

<style lang="scss" scoped>
#main {
  padding: 1rem;
  flex: 1 1 auto;
  overflow: auto;
}
</style>
