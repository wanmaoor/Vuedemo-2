<template>
  <div id="app3">
    <nav>
      <router-link to="/Home">Home</router-link>
      <router-link to="/About">About</router-link>
    </nav>
    <router-view></router-view>
  </div>
</template>

<script>
	import Vue from 'vue'
	import VueRouter from 'vue-router'

	Vue.use(VueRouter)
	const Home = {
		// eslint-disable-next-line no-mixed-spaces-and-tabs
		template: `<div>Home</div>`
	}
	const About = {template: `<div>About</div>`};
	const router = new VueRouter({
		routes: [
			{path: '/home', component: Home},
			{path: '/about', component: About}
		]
	})
	export default {
		name: "VueRouter",
		router,
    Home,
    About
	}
</script>

<style scoped>

</style>