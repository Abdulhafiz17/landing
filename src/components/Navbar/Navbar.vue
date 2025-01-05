<script>
export default {
  name: "Navbar",
  data() {
    return {
      shadow: false,
    };
  },
  computed: {
    main_div() {
      return document.querySelector("#main");
    },
  },
  mounted() {
    this.main_div.onscroll = (event) => {
      const element = event.target;
      const scroll_top = element.scrollTop;
      if (scroll_top) {
        this.shadow = true;
      } else {
        this.shadow = false;
      }
    };
  },
};
</script>

<template>
  <nav :class="{ shadow: shadow }">
    <router-link to="#profile" :class="{ active: $route.hash == '#profile' }">
      <i class="fa fa-user"></i>
    </router-link>
    <router-link to="#services" :class="{ active: $route.hash == '#services' }">
      <i class="fa fa-code-branch"></i>
    </router-link>
    <!-- <router-link to="#about" :class="{ active: $route.hash == '#about' }">
      <i class="fa fa-info-circle"></i>
    </router-link> -->
  </nav>
</template>

<style lang="scss" scoped>
nav {
  position: absolute;
  top: 50%;
  left: 0;
  padding: 5px;
  // width: 100%;
  display: flex;
  flex-direction: column;
  place-content: center;
  gap: 5px;
  background-color: var(--transparent-background);
  backdrop-filter: blur(2px);
  border: thin solid rgb(0, 130, 255);
  border-left: none;
  border-radius: 0 10px 10px 0;
  transform: translateY(-50%);
  transition: all 0.3s;
  font-size: 20px;
  z-index: 1;

  &.shadow {
    box-shadow: 0 0 5px 10px rgb(0, 130, 255, 0.1);
  }

  a {
    padding: 5px 10px;
    width: 100%;
    color: rgb(0, 130, 255);
    border-radius: 5px;
    text-align: center;
    text-decoration: none;
    transition: all 0.2s;

    &.active {
      color: black;
      background-color: rgb(0, 130, 255);
    }

    &:hover {
      // scale: 1.2;
      filter: drop-shadow(0 0 10px rgb(0, 130, 255));
    }
  }
}
</style>
