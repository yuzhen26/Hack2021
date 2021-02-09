<template>
  <div id="iconsList">
    <ul>
      <li v-for="icon in iconsList" :key="icon.id">
        <div class="pic">
          <img id="borderimg2" v-bind:src="icon.imageURL" border="1" />
          <div class="centered">{{ icon.name }}</div>
        </div>
      </li>
    </ul>
    <div id="footer">@2021 by Merlin<br>merlin_tours@info.com</div>
  </div>
</template>

<script>
export default {
  props: {
    iconsList: {
      id: String,
      name: String,
      imageURL: String,
    },
  }
}


</script>

<style scoped>
#iconsList {
  width: 100%;
  max-width: 100%;
  margin: 0px;
  padding: 0 5px;
  box-sizing: border-box;
  width: 100%;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
  height: 100%;
  width: 100%;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 10px;
  margin: 10px;
}
#borderimg2 {
  width: 300px;
  height: 300px;
}

#footer {
  background-color: plum ;
  height: 50px;
  font-size: 15px;
  text-align: center;
  padding-top: 10px;
  color:white;
}
</style>