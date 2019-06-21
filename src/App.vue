<template>
  <div id="app">
    <section>
      <AddOne />
    </section>
  </div>
</template>

<script>
import AddOne from  "./components/AddOne";

export default {
  name: "App",
  components: {
    AddOne
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
