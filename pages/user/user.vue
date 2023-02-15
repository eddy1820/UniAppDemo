<template>
	<view>
		<button @click="add">add bage</button>
		<button @click="remove">remove bage</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {

			}
		},
		methods: {
			add() {
				uni.setTabBarBadge({
					index: 1,
					text: "5"
				})
			},
			remove() {
				uni.removeTabBarBadge({
					index: 1
				})
			}
		},
		onLoad() {
			uni.setTabBarBadge({
				index: 1,
				text: "3"
			})
		}
	}
</script>

<style>

</style>
