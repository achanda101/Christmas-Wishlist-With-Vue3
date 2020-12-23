<template>
  <div>
    <img alt="Santa Claus Graphic" src="./assets/santa_icon.png" height="150"/>
    <WishList />
    <!-- <HelloWorld msg="Welcome to Vodkarani's Lair!" /> -->
  </div>
</template>

<script>
import WishList from "./components/wishList.vue";

export default {
  name: "App",
  components: {
    WishList
  }
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
