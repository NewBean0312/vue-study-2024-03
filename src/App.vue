<template>
  <div class="black-bg" v-if="modalState == true">
    <div class="white-bg">
      <h4>상세 페이지</h4>
      <p>상세 페이지 내용</p>
      <button @click="modalState = false">닫기</button>
    </div>
  </div>
  <div class="menu">
    <a v-for="(menu, i) in menuData" :key="i">{{ menu }}</a>
  </div>
  <div>
    <img src="./assets/room0.jpg" class="room-img" />
    <h4 @click="modalState = true">{{ productData[0] }}</h4>
    <p>50만원</p>
    <button @click="increase1">허위매물신고</button>
    <span> 신고 수 : {{ declareNo[0] }}</span>
  </div>
  <div>
    <img src="./assets/room1.jpg" class="room-img" />
    <h4>{{ productData[1] }}</h4>
    <p>60만원</p>
    <button @click="increase2">허위매물신고</button>
    <span> 신고 수 : {{ declareNo[1] }}</span>
  </div>
  <div>
    <img src="./assets/room2.jpg" class="room-img" />
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
      // 데이터 보관 (데이터는 object 자료형으로 저장)(state라고도 불림)
      modalState: false,
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
body {
  margin: 0;
}

div {
  box-sizing: border-box;
}

.black-bg {
  position: fixed;
  padding: 20px;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,0.5);
}

.white-bg {
  padding: 20px;
  width: 100%;
  border-radius: 8px;
  background-color: #fff;
}

.room-img {
  width: 100%;
  margin-top: 40px;
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
  color: #fff;
  padding: 10px;
}
</style>
