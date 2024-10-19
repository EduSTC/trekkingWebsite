<script>

export default {
  data() {
    return {
      MenuOpen: false
    }
  },
  methods: {
    showMenu() {
      this.MenuOpen = !this.MenuOpen;
      console.log(this.MenuOpen)
    }
  }
}
</script>


<template>
  <div id="title-container">
    <a href=""><img src="../assets/robota-logo.svg" id="robota-logo"></a>
    <h1 id="header-title">ROBOTA</h1>
    <h1 id="header-sub-title">Trekking</h1>
  </div>
  <nav tabindex="0">
    <ul :class="{displayMenu : MenuOpen}" role="menubar" aria-haspopup="true">
        <li role="menuitem" aria-label="Heatmap"><a href="">Heatmap</a></li>
        <li role="menuitem" aria-label="Sensors"><a href="">Sensors</a></li>
        <li role="menuitem" aria-label="Control"><a href="">Control</a></li>
        <li role="menuitem" aria-label="Power"><a href="">Power</a></li>
    </ul>
    <div id="hamburguer-container" @click="showMenu">
      <span></span>
      <span></span>
      <span></span>
    </div>
  </nav>
</template>


<style scoped>

  #title-container {
    display: flex;
    align-items: center;
    gap: 1rem;

    a {
      img {
        height: 3rem;
      }
    }
    h1 {
      @media screen  and (max-width: 760px) {
        font-size: 1.5rem;
      }
    }
    #header-title {
      background-image: linear-gradient(to right, purple , orange);
      color: transparent;
      background-clip: text;
    }
    #header-sub-title {
      color: white;
    }
  }

  nav {
    display: flex;
    align-items: center;


    ul {
      margin: 0 2rem;
      display: flex;
      gap: 1rem;
      list-style-type: none;
      padding: 0;

      @media screen  and (max-width: 760px) {
        display: none;
        position: absolute;
        top: calc(4rem + 1px);
        left: 0;
        right: 0;
        background-color: #444;
        flex-direction: column;
        z-index: 1;
        border-radius: 3px;
        padding: 5px;
        margin: 1px;
        align-items: center;
      }
    }

    .displayMenu {
      display: flex;
    }

    a {
      text-decoration: none;
      font-size: 20px;
      color: white;
    }
    a:hover {
      background-clip: text;
      background-image: linear-gradient(to right, purple , orange);
      color: transparent;
    }
    #hamburguer-container {
      display: flex;
      cursor: pointer;
      flex-direction: column;
      justify-content: space-around;
      width: 2rem;
      height: 2rem;
      span {
        display: block;
        width: 100%;
        height: 3px;
        background-color: #ffffff;
      }
      @media screen  and (min-width: 760px) {
        display: none;
      }
    }
    
  }
  
</style>