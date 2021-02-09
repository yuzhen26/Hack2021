<template>
  <div id="app">
    <header>
      Let's Travel
      <span id="taskbar">Home | Eat | Relax | SightSee | About </span>
    </header>
    <div class="container">
      <img id="borderimg" border=1>
      <div class="centered">Escape The Ordinary</div>
    </div>
    <HomePage v-bind:iconsList = "iconsList"></HomePage>
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue'

export default {
  name: 'App',
  components: {
    HomePage,
  },
  data() {
    return {
      iconsList: [
        {
          id: "#000",
          name: "EAT",
          imageURL:
            "https://www.ephotozine.com/articles/6-awesome-travel-food-photography-tips-for-that-perfect-instagram-shot-16756/images/xlg_64361570_10157067569056047_5751272624537731072_n.jpg",
          page: 
            "SightSee.html",
        },
        {
          id: "#025",
          name: "RELAX",
          imageURL:
            "https://i.pinimg.com/736x/cb/ea/08/cbea0801c97d18fcb596d7b1dc289b5a.jpg",
          page: 
            "SightSee.html",
        },
        {
          id: "#067",
          name: "SIGHTSEE",
          imageURL:
            "https://i.pinimg.com/originals/ab/a3/02/aba3022556093409efbdc2edb69d5a46.jpg"
        }
      ],
      
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
  height: 40px;
  top: 0px;
  font-size: 30px;
  text-align: left;
  font-family: monospace;
}

#borderimg {
  background-image: url(https://www.oakbaynews.com/wp-content/uploads/2019/05/16863896_web1_2070413.jpg);
  width: 100%;
  height: 500px;
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

#taskbar {
  margin-left: 30%;
}

</style>
