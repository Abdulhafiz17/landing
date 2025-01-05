<script>
export default {
  name: "Profile",
  computed: {
    years() {
      return new Date().getFullYear() - 2004;
    },
  },
};
</script>

<template>
  <main>
    <div class="row">
      <div class="col-md-6">
        <span>
          <span>Web Developer</span>
          <br />
          <span>Abdulhafiz Mahmud</span>
        </span>
      </div>
      <div class="col-md-6"></div>
    </div>
    <div class="links">
      <a href="https://www.instagram.com/abdulhafiz_082" class="instagram">
        <i class="fab fa-instagram"></i>
        abdulhafiz_082
      </a>
      <a href="https://t.me/abdulhafiz_mahmud" class="telegram">
        <i class="fab fa-telegram"></i>
        abdulhafiz_mahmud
      </a>
      <a href="https://github.com/Abdulhafiz17" class="github">
        <i class="fab fa-github"></i>
        Abdulhafiz17
      </a>
      <a href="mailto:@abdo.maxmud" class="github">
        <i class="far fa-envelope"></i>
        abdo.maxmud
      </a>
      <a href="tel:+998936486046" class="github">
        <i class="fa fa-phone"></i>
        +998 93 648 60 46
      </a>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main {
  height: 100%;

  .row {
    height: 90%;
  }

  .col-md-6:nth-child(1) {
    flex: 1 1 auto;
    display: flex;
    place-content: center;
    place-items: center;
    border-radius: 5px 50px 50px 5px;
    font-size: 3rem;
    font-weight: 700;
    background: -webkit-linear-gradient(
      left,
      var(--main-text),
      var(--main-color)
    );
    background-clip: text;
    -webkit-text-fill-color: transparent;
  }

  .links {
    height: max-content;
    display: flex;
    flex-wrap: wrap;
    place-content: center;
    place-items: center;
    gap: 1rem;
    font-size: large;

    i {
      margin: 0 5px;
    }

    span,
    a {
      padding: 5px 1rem;
      font-weight: bold;
      color: var(--main-text);
      text-decoration: none;
      transition: all 0.3s;

      &.instagram {
        background: -webkit-linear-gradient(70deg, #f9ce34, #ee2a7b, #6228d7);
        background-clip: text;
        -webkit-text-fill-color: transparent;
      }

      &.telegram {
        color: rgb(36, 152, 201);
        // background: -webkit-linear-gradient(left, #002e6f, #f2fcfe);
        // background-clip: text;
        // -webkit-text-fill-color: transparent;
      }
    }
  }
}
</style>
