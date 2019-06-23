<template>
  <div id="app">
    <nav>
      <router-link to="/increment" class="nav">常規方法自加</router-link>
      <router-link to="/directive" class="nav">自定義指令</router-link>
      <router-link to="/router" class="nav">vue-router入門</router-link>
      <router-link to="/user" class="nav">動態路由匹配</router-link>
    </nav>
    <router-view class="view"></router-view>
  </div>
</template>

<script>
import vuerouter from "vue-router";
import Vue from "vue";
import AddOne from "./components/AddOne";
import Directive from "./components/Vue.directive";
import VueRouter from "./components/VueRouter";
import DynamicRoute from "./components/DynamicRouteMatching";
import Err from "./components/Error";

Vue.use(vuerouter);

const router = new vuerouter({
  routes: [
    { path: "/increment", component: AddOne },
    { path: "/directive", component: Directive },
    { path: "/router", component: VueRouter },
    { path: "/user/:id", component: DynamicRoute },
    { path: "*", component: Err }
  ]
});

export default {
  name: "App",
  components: {
    AddOne,
    Directive,
    VueRouter,
    DynamicRoute
  },
  router
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
hr {
  width: 50%;
}

section {
  width: 50%;
  height: 20vh;
  text-align: center;
  margin: 1vh auto;
  border: 1px solid black;
}
nav {
  display: flex;
  flex-direction: row;
  justify-content: center;
}
.nav {
  text-decoration: none;
  color: black;
  margin: 5px auto;
}
.nav:active {
  color: #333;
}
.nav:visited {
  color: yellowgreen;
}
.view {
  padding: 20vh;
}
</style>
