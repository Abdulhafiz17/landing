<script>
export default {
  name: "Services",
};
</script>

<template>
  <main>
    <div class="row">
      <div class="col-md-6">
        <ul class="services-list">
          <li class="item">
            <span class="title">Website Development</span>
            <p>
              Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat,
              et.
            </p>
          </li>
          <li class="item"></li>
          <li class="item">
            <span class="title">Businnes automatization</span>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
              Voluptatibus quidem cum numquam maiores earum vitae enim
              necessitatibus voluptatum? Vero, aut?
            </p>
          </li>
          <li class="item"></li>
          <li class="item">
            <span class="title">Telegram bot</span>
            <p>
              Lorem ipsum dolor sit, amet consectetur adipisicing elit.
              Voluptatibus quidem cum numquam maiores earum vitae enim
              necessitatibus voluptatum? Vero, aut?
            </p>
          </li>
        </ul>
      </div>
      <div class="col-md-6">
        <div class="skills">
          <div class="item">
            <img src="../../assets/icons/html.png" alt="html" />
            <img src="../../assets/icons/css.png" alt="css" />
            <span class="title">HTML + CSS</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/scss.png" alt="scss" />
            <span class="title">SCSS</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/bootstrap.png" alt="bootstrap" />
            <span class="title">Bootstrap</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/js.png" alt="js" />
            <span class="title">JavaScript</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/vue.png" alt="vue" />
            <span class="title">Vue JS</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/react.png" alt="react" />
            <span class="title">React</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/vite.png" alt="vite" />
            <span class="title">Vite</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/webpack.png" alt="webpack" />
            <span class="title">Webpack</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/mysql.png" alt="mysql" />
            <span class="title">MySQL</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/node.png" alt="node" />
            <span class="title">Node JS</span>
          </div>
          <div class="item">
            <img src="../../assets/icons/android.png" alt="android" />
            <span class="title">Android</span>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
main {
  width: 100%;
  height: 100%;

  .row {
    height: 100%;

    .col-md-6 {
      padding: 1rem;
    }
  }

  .services-list {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    place-content: center;
    place-items: center;
    list-style: none;

    .item {
      min-height: 50px;
      border: thin solid var(--main-color);
    }

    .item:nth-child(odd) {
      position: relative;
      margin: 0 0 0 3rem;
      padding: 1rem 2rem;
      width: calc(100% - 3rem);
      place-self: start;
      border-radius: 1rem;

      .title {
        color: white;
        font-size: x-large;
        font-weight: bold;
      }

      p {
        margin: 0;
      }

      @media (max-width: 768px) {
        & {
          margin: 0;
          width: 100%;
        }
      }
    }
  }

  .skills {
    width: 100%;
    height: 100%;
    display: flex;
    flex-wrap: wrap;
    place-content: center;
    place-items: center;
    gap: 1rem;

    .item {
      position: relative;
      padding: 10px;
      border: thin solid transparent;
      border-radius: 10px;
      transition: all 0.3s;

      &:hover {
        background-color: var(--secondary-background);
        border-color: black;

        .title {
          opacity: 1;
        }
      }

      img {
        width: 100px;
      }

      .title {
        position: absolute;
        bottom: 0;
        left: 0;
        padding: 5px;
        width: 100%;
        background-color: var(--transparent-background);
        backdrop-filter: blur(2px);
        border-radius: 0 0 10px 10px;
        text-align: center;
        font-weight: bold;
        opacity: 0;
        transition: all 0.3s;
      }
    }
  }
}
</style>
