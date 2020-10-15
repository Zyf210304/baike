<template>
	<view>
		<view class="box">
			<view class="box-item">1</view>
			<view class="box-item">2</view>
			<view class="box-item">3</view>
			<view class="box-item">4</view>
			<view class="box-item">5</view>
			<view class="box-item">6</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.box {
	width: 100%;
	/* 高度不写死 item高度就不会被压缩 view就会自动扩充高度填满*/
	/* height: 500upx; */
	border: 1upx solid #CCCCCC;
	/* 同一行显示 */
	display: flex; 
	/* 自动换行  wrap-reverse 倒叙换行*/
	flex-wrap: wrap;
	/* justify-content 水平方向 center space-between  flex-end*/
	justify-content: space-between;
	/* align-items 竖直方向 center stretch(竖直方向填充满 不要设置子元素高度) flex-end*/
	align-items: center;
	
	/* 排列方式 column 先上下  row先水平 */
	/* flex-direction: column; */
	
	
}
.box-item {
	color: #FFFFFF;
	/* width: 200upx;*/
	/* width: 50%;*/
	/* flex: 1; */
	height: 200upx;
	/* line-height: 200upx; */
	font-size: 30upx;
	font-weight: bold;
	text-align: center;
	
	display: flex;
	align-items: center;
	justify-content: center;
	
}
.box-item:nth-of-type(odd) {
	background: #09BB07;
}
.box-item:nth-of-type(even) {
	background: #8A6DE9;
}
.box-item:first-of-type {
	/* 0不被压缩 */
	flex-shrink: 0;
}
.box-item:nth-of-type(3n -1) {
	width: 50%;
	/* flex: 2; */
}
.box-item:nth-of-type(3n -2) {
	width: 20%;
	/* flex: 1; */
}
.box-item:nth-of-type(3n) {
	width: 20%;
	/* flex: 1; */
}

 </style>
