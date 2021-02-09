<template>
    <div>
    <ul>
      <li v-for="place in placesList" :key="place.id">
        <div class="pic">
          <span>{{ place.name }}</span>
          <img id="borderimg2" v-bind:src="place.imageURL" border="1" />         
        </div>
      </li>
    </ul>
    </div>
</template>

<script>
export default {};
</script>

<style scoped>
</style>