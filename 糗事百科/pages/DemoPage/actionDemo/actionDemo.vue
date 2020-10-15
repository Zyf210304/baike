<template>
	<view>
		<view class="font">
			{{name}}
		</view>
		<view class="box" @click="clickEvent">
			按钮
		</view>
		
		
		<view class="box1"  @click="outEvent">
			<!-- 外面 -->
			<view class="box2" @click.stop="inEvent">
				里面
			</view>
		</view>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				name:"哈哈哈"
			}
		},
		methods: {
			clickEvent() {
				console.log("点击了");
				this.name = "嘻嘻";
			},
			inEvent(){
				console.log("里面被点击");
			},
			outEvent(){
				console.log("外面被点击");
			}
		}
	}
</script>

<style>
.font {
	font-size: 50upx;
	border: 1upx solid #007AFF;
	padding: 20upx;
	text-align: center;
}
.box {
	background: #09BB07;
	color: #FFFFFF;
	width: 80%;
	margin: auto;
	height: 80upx;
	font-size: 50upx;
	border-radius: 16upx;
	border: 1upx solid #EEEEEE;
	display: flex;
	justify-content: center;
	align-items: center;
}
.box1 {
	width: 100%;
	height: 100upx;
	background: #09BB07;
	color: #FFFFFF;
	display: flex;
	justify-content: center;
	align-items: center;
}
.box2 {
	width: 50%;
	height: 50upx;
	background: #8A6DE9;
	display: flex;
	justify-content: center;
	align-items: center;
}
</style>
