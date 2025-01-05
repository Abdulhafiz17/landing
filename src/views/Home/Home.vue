<script>
import Profile from "@/components/Home/Profile.vue";
import Services from "@/components/Home/Services.vue";
import About from "@/components/Home/About.vue";
export default {
  name: "Home",
  components: { Profile, Services, About },
  computed: {
    mobile() {
      if (window.innerHeight <= 768) {
        return true;
      } else {
        return false;
      }
    },
    content() {
      return this.$route.hash;
    },
  },
};
</script>

<template>
  <div v-if="mobile">
    <Profile />
    <hr />
    <Services />
  </div>
  <Transition name="content" mode="out-in" v-else>
    <Profile v-if="content == '#profile'" />
    <Services v-else-if="content == '#services'" />
  </Transition>
</template>

<style scoped>
.content-enter-active,
.content-leave-active {
  transition: all 0.3s;
}

.content-enter-from,
.content-leave-to {
  opacity: 0;
}
</style>
