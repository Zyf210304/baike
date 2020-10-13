<template>
	<view>
		<view class="view-box animated " hover-class="view-box-hover rubberBand" hover-stay-time="2000">
			view
		</view>
		
		<text :selectable="true">
			这&nbsp;&nbsp;&nbsp;是text\n第二行
		</text>
		
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
.view-box {
	width: 200upx;
	height: 200upx;
	background-color: #007AFF;
	color: #FFFFFF;
	margin: 100upx;
}
.view-box-hover{
	background-color: #FF3333;
}
</style>
