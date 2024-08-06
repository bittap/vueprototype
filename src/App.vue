<template>
  <div class="menu">
    <a v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>
  <div>
    {{ logo }}
    <h4 :style="style">{{ products[0] }}</h4>
    <p>{{ price1 }}万円</p> 
  </div>
  <div>
    <h4>{{ products[1] }}</h4>
    <p>{{ price2 }}万円</p> 
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      logo: "ワンルームショップ",
      price1: 60,
      price2: 70,
      style: "color : blue",
      products: ["aaa", "bbb", "ccc"],
      menus: ["home", "product", "about"],
    };
  },
  components: {},
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.menu {
  background: darkslateblue;
  padding: 15px;
  border-radius: 5px;
}

.menu a {
  color: white;
  padding: 10px;
}
</style>
