<template>
  <div>
    <p>{{num}}</p>
    <button @click="addOne">addOne</button>
    <p>常規方法自加</p>
  </div>
</template>

<script>
	export default {
		name: "AddOne",
    data(){
			return {
				num: 0
      }
    },
    methods: {
			addOne(){
				return this.num++
      }
    }
	}
</script>

<style scoped>

</style>