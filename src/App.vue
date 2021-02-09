<template>
  <div id="app">
    <header>Let's Go</header>
    <div class="container">
      <img id="borderimg" border=1>
      <div class="centered">Escape The Ordinary</div>
    </div>
    <HomePage v-bind:iconsList = "iconsList"></HomePage>
    <SightSee v-bind:placesList = "placesList"></SightSee>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'
import SightSee from './components/SightSee.vue'

export default {
  name: 'App',
  components: {
    HomePage,
    SightSee
  },
  data() {
    return {
      iconsList: [
        {
          id: "#000",
          name: "EAT",
          imageURL:
            "https://www.ephotozine.com/articles/6-awesome-travel-food-photography-tips-for-that-perfect-instagram-shot-16756/images/xlg_64361570_10157067569056047_5751272624537731072_n.jpg"
        },
        {
          id: "#025",
          name: "RELAX",
          imageURL:
            "https://i.pinimg.com/736x/cb/ea/08/cbea0801c97d18fcb596d7b1dc289b5a.jpg"
        },
        {
          id: "#067",
          name: "SIGHTSEE",
          imageURL:
            "https://i.pinimg.com/originals/ab/a3/02/aba3022556093409efbdc2edb69d5a46.jpg"
        }
      ],
      placesList: [
        {
          name: "Taj Mahal",
          imageURL: 
            "https://www.planetware.com/photos-large/IND/india-top-attractions-taj-mahal.jpg"
        },
        {
          name: "London Eye",
          imageURL: 
            "https://media.cntraveler.com/photos/55c8be0bd36458796e4ca38a/16:9/w_2560%2Cc_limit/london-eye-2-cr-getty.jpg"
        }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

header {
  color: #957dad;
  height: 50px;
  font-size: 30px;
  text-align: center;
  font-family: monospace;
}

#borderimg {
  background-image: url(https://www.oakbaynews.com/wp-content/uploads/2019/05/16863896_web1_2070413.jpg);
  width: 100%;
  height: 700px;
  background-size: 100% 100%;
}

.container {
  position: relative;
  text-align: center;
  font-size: 30px;
  font-family: monospace;
  font-weight: bold;
  color: white;
}

.centered {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: 50px;
}

.pic {
   position: relative;
  text-align: center;
  font-size: 30px;
  font-weight: bolder;
  color: white;
  font-family:monospace;

}

</style>
