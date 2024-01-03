<template>
	<view>
		<button type="primary" @click="button1">异步获取系统信息</button>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			button1()
			{
				uni.getSystemInfo({
					success: (data) => {
						console.log(data);
					},
					fail: (err) => {
						console.log("获取失败");
					}
				})
			}
		}
	}
</script>

<style>

</style>
