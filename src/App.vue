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
    <img :src="oneRoomData[0].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[0].title }}</h4>
    <p>{{ oneRoomData[0].price}}</p>
  </div>
  <div>
    <img :src="oneRoomData[1].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[1].title }}</h4>
    <p>{{ oneRoomData[1].price}}</p>
  </div>
  <div>
    <img :src="oneRoomData[2].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[2].title }}</h4>
    <p>{{ oneRoomData[2].price}}</p>
  </div>
  <div>
    <img :src="oneRoomData[3].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[3].title }}</h4>
    <p>{{ oneRoomData[3].price}}</p>
  </div>
  <div>
    <img :src="oneRoomData[4].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[4].title }}</h4>
    <p>{{ oneRoomData[4].price}}</p>
  </div>
  <div>
    <img :src="oneRoomData[5].image" class="room-img" />
    <h4 @click="modalState = true">{{ oneRoomData[5].title }}</h4>
    <p>{{ oneRoomData[5].price}}</p>
  </div>
</template>

<script>
import oneRoom from './assets/oneRoom';

export default {
  name: "App",
  data() {
    return {
      // 데이터 보관 (데이터는 object 자료형으로 저장)(state라고도 불림)
      oneRoomData: oneRoom,
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
  background-color: rgba(0, 0, 0, 0.5);
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
