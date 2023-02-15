<template>
	<view class="container">
		<view class="title">
			{{this.user.title}}
		</view>
		<view class="row">
			<view>Name:</view>
			<view>{{this.user.name}}</view>
		</view>
		<view class="row">
			<view>Age:</view>
			<view>{{this.user.age}}</view>
		</view>

		<button class="btn" @click="onClick">to parent</button>
	</view>
</template>

<script>
	export default {
		name: "homeInfo",
		props: {
			title: {
				type: String,
				default: "默认标题"
			},
			arr: {
				type: Array,
				default () {
					return [1, 2, 3]
				}
			},
			user: {
				type: Object,
				default () {
					return {
						name: "null",
						age: 0
					}
				}
			}
		},
		data() {
			return {

			};
		},
		methods: {
			onClick() {
				this.$emit("onViewBtnClick", this.user)
			}
		}
	}
</script>

<style lang="scss">
	.container {
		border: solid orangered 30rpx;
		font-size: 40rpx;
		color: darkred;
		background: yellowgreen;
		padding: 20rpx;

		.title {
			font-size: 60rpx;
			color: blue;
			align-items: center;
		}

		.row {
			flex-direction: row;
		}

		.btn {
			margin-top: 40rpx;
			width: 200rpx;
			background: yellow;
		}
	}
</style>
