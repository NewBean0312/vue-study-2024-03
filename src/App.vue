<template>
  <div class="menu">
    <a v-for="(menu, i) in menuData" :key="i">{{ menu }}</a>
  </div>
  <div  v-for="(product, i) in productData" :key="i">
    <h4>{{ productData[i] }}</h4>
    <p>50 만원</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // 데이터 보관 (데이터는 object 자료형으로 저장)
      menuData : ["Home", "Shop", "About"],
      productData: ["역삼동원룸", "천호동원룸", "마포구원룸"],
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
  color: #fff;
  padding: 10px;
}
</style>
