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
			color: {
				bind(){
					console.log('1 - bind')
        },
        inserted(el, binding){
	        console.log('2 - inserted')
					el.style = `color: ${binding.value}`
        },
        update(){
					console.log('3 - update')
        },
        componentUpdated(){
					console.log('4 - comopnentUpdated')
        }
      }
		}
	}
</script>

<style scoped>

</style>