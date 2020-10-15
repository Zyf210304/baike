<template>
	<view>
		<!-- 循环1维数组 -->
		111
		<view class="font" v-for="(value,index) in list1" :key = "index">
			{{index}}-{{value}}
		</view>
		
		<view class="font" v-for="(value, index) in list2"  :key = "index">
			{{value.id}}-{{value.name}}
		</view>
		<view class="font" v-for="(value, index1) in list3"  :key = "index1">
			{{value.name}}
			<view class="font2" v-for="(val, index) in value.list"  :key = "index">
				{{val}}
			</view>
		</view>
		
		<view class="font" v-for="(val, key) in object" :key = "key">
			{{key}}:{{val}}
		</view>
		
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				list1:["篮球","足球","乒乓球"],
				list2:[
					{id:"11", name:"篮球"},
					{id:"22", name:"足球"},
					{id:"33", name:"乒乓球"},
				],
				list3:[
					{name:"河南",
					list:["郑州", "漯河", "焦作"]},
					{name:"浙江",
					list:["杭州", "金华", "衢州"]}
				],
				object:{
					"name":"河南",
					"capital":"郑州",
				}
			}
		},
		methods: {
			
		}
	}
</script>

<style>
.font {
	font-size: 40upx;
}
</style>
