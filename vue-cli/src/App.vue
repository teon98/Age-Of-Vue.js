<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <!-- 컴포넌트 태그를 등록한 것과 같다.-->
    <HelloWorld v-bind:msg="message" />
    <!-- 컴포넌트 명명법 종류 -->
    <!--
      <hello-world></hello-world>
      <HelloWorld></HelloWorld>
      <HelloWorld/>
    -->
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';

export default {
  // 인스턴스 옵션 속성 or 컴포넌트 옵션 속성
  name: 'App',
  data() {
    return { message: '안녕' };
  },
  components: {
    HelloWorld,
  },
  props: {
    //배열로 전달해줬던 props값을 props validation으로 type까지 보낸다.
    msg: String,
  },
};
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
</style>
