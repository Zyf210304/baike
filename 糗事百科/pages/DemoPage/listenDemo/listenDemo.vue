<template>
	<view>
		
		<view class="font">
			{{name}}
		</view>
		<button type="default" @click="changeEvent">修改数值</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name:"一个名称",
				count:1,
			}
		},
		methods: {
			changeEvent(){
				this.name = this.count++;
			}
		},
		watch: {
			name(val){
				console.log(val);
			}
		}
	}
</script>

<style>
.font {
	font-size: 50upx;
	text-align: center;
}
</style>
