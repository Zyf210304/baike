<template>
	<view>
		<view class="font">
			{{changeWeight}}
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				weight:200,
			}
		},
		methods: {
			
		},
		computed: {
			changeWeight() {
				return this.weight > 1000 ? this.weight / 1000 + 'kg' : this.weight + 'g';
			}
		}
	}
</script>

<style>

</style>
