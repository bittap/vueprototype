<template>
  <div class="menu">
    <a v-for="(menu, i) in menus" :key="i">{{ menu }}</a>
  </div>

  <div class="black-bg" v-if="modal_opend == false">
    <div class="white-bg">
      <h4>詳細ページ</h4>
      <p>ページ内容</p>
    </div>
  </div>

  <div>
    <h4 @click="modal_opend = true">ワンルーム</h4>
  </div>

  <div v-for="(product, i) in products" :key="i">
    <img :src="product.image" />
    <h4>{{ product.title }}</h4>
    <p>{{ product.price }}</p>
  </div>
</template>

<script>
import data from "./assets/oneroom.js";

export default {
  name: "App",
  data() {
    return {
      modal_opend: true,
      logo: "ワンルームショップ",
      price1: 60,
      price2: 70,
      style: "color : blue",
      products: data,
      menus: ["home", "product", "about"],
    };
  },
  methods: {
    increase() {
      this.count++;
    },
  },
  components: {},
};
</script>

<style>
body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0);
  position: fixed;
  padding: 20px;
}

.white-bg {
  width: 100%;
  background: white;
}

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
