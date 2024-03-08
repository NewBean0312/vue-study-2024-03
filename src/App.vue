<template>
  <div class="menu">
    <a v-for="(menu, i) in menuData" :key="i">{{ menu }}</a>
  </div>
  <div>
    <h4>{{ productData[0] }}</h4>
    <p>50만원</p>
    <button @click="increase1">허위매물신고</button>
    <span> 신고 수 : {{ declareNo[0] }}</span>
  </div>
  <div>
    <h4>{{ productData[1] }}</h4>
    <p>60만원</p>
    <button @click="increase2">허위매물신고</button>
    <span> 신고 수 : {{ declareNo[1] }}</span>
  </div>
  <div>
    <h4>{{ productData[2] }}</h4>
    <p>70만원</p>
    <button @click="increase3">허위매물신고</button>
    <span> 신고 수 : {{ declareNo[2] }}</span>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      // 데이터 보관 (데이터는 object 자료형으로 저장)
      declareNo: [0, 0, 0],
      menuData: ["Home", "Shop", "About"],
      productData: ["역삼동원룸", "천호동원룸", "마포구원룸"],
    };
  },
  methods: {
    increase1() {
      this.declareNo[0]++; // 함수 안에서 데이터를 쓸 경우, this.데이터명
    },

    increase2() {
      this.declareNo[1]++;
    },

    increase3() {
      this.declareNo[2]++;
    },
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
