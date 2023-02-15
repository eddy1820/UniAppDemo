<template>
	<view>
		<view class="item">
			<button class="btn" @click="onClick">close</button>
			<view class="dialog" :style="{height: status? '300rpx':'0rpx'}"></view>
		</view>
	</view>
</template>

<script>
	export default {
		name: "myitem",
		props: {
			status: false
		},
		data() {
			return {};
		},
		methods: {
			onClick() {
				this.$emit("update:status",false)
			}
		}
	}
</script>

<style lang="scss">
	.item {
		width: 750rpx;
		height: 500rpx;
		background: skyblue;
		border-radius: 20rpx;

		.btn {
			width: 300rpx;
			margin-top: 30rpx;
			background: palegreen;
		}

		.dialog {
			width: 500rpx;
			background: orangered;
		}
	}
</style>
