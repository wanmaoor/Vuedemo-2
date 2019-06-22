<template>
  <div id="app">
    <section>
      <AddOne />
    </section>
    <section>
      <Directive />
    </section>
    <section>
      <VueRouter />
    </section>
  </div>
</template>

<script>
import AddOne from  "./components/AddOne";
import Directive from "./components/Vue.directive"
import VueRouter from "./components/VueRouter"

export default {
  name: "App",
  components: {
    AddOne,
    Directive,
    VueRouter
  }
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
  hr{
    width: 50%;
  }

  section{
    width: 50%;
    height: 15vh;
    text-align: center;
    margin: 1vh auto;
    border: 1px solid black;

  }
</style>
