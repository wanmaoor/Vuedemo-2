<template>
  <div>
    <p v-color="color">{{num}}</p>
    <button @click="addOne">addOne</button>
    <p>自定義指令, 將顔色設置爲綠色</p>
  </div>
</template>

<script>
	export default {
		name: "AddOne",
		data(){
			return {
				num: 0,
        color: 'green'
			}
		},
		methods: {
			addOne(){
        this.num++
			}
		},
		//自定义指令
		directives: {
			color(el, binding){
				el.style = `color: ${binding.value}`
      }
		}
	}
</script>

<style scoped>

</style>