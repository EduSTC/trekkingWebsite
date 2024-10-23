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
    <div id ="sensor-container">
        <h2>Sensors</h2>
        <nav tabindex="0">
        <ul role="menubar" aria-haspopup="true">
            <li role="menuitem" aria-label="Sensor1"><a href="">Sensor1</a></li>
            <li role="menuitem" aria-label="Sensor2"><a href="">Sensor2</a></li>
            <li role="menuitem" aria-label="Sensor3"><a href="">Sensor3</a></li>
            <li role="menuitem" aria-label="Sensor4"><a href="">Sensor4</a></li>
            <li role="menuitem" aria-label="Sensor5"><a href="">Sensor5</a></li>
            <li role="menuitem" aria-label="Sensor6"><a href="">Sensor6</a></li>
            <li role="menuitem" aria-label="Sensor7"><a href="">Sensor7</a></li>
            <li role="menuitem" aria-label="Sensor8"><a href="">Sensor8</a></li>
            <li role="menuitem" aria-label="Sensor9"><a href="">Sensor9</a></li>
            <li role="menuitem" aria-label="Sensorl0"><a href="">Sensor10</a></li>
        </ul>
        </nav>
    </div>
  </template>
<style scoped>
    #sensor-container {
        display: flex;
        flex-direction: column;
        background-color: rgb(26, 26, 26);
        border: 1px solid grey;
        border-radius: 3px;
        text-align: center;
        padding: 1rem;

        @media screen  and (max-width: 810px) {
            font-size: 0.5rem;
        }
        h2 {
        margin: 0;
        margin-bottom: 1rem;
        font-size: 1.5rem;
        color: white;
        border-bottom: 1px solid grey;
        }
        ul {
            list-style-type: none;
            padding: 0;
            a {
            text-decoration: none;
            font-size: 1.5rem;
            color: grey;
            }
            a:hover {
            background-clip: text;
            background-image: linear-gradient(to right, purple , orange);
            color: transparent;
            }

            li {
                padding-bottom: 3px;
            }
        }

    }
    


</style>