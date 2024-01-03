<template>
	<view>
		<button type="primary" @click="button1">异步获取系统信息</button>
		<button type="primary" @click="button2">同步获取系统信息</button>
		<button type="primary" @click="button3">获取设备基础信息</button>
		<button type="primary" @click="button4">获取窗口信息</button>
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
			},
			button2()
			{
				const info= uni.getSystemInfoSync();
				console.log(info);
			},
			button3()
			{
				const info= uni.getDeviceInfo();
				console.log(info);
			},
			button4()
			{
				const info= uni.getWindowInfo();
				console.log(info);
			}
		}
	}
</script>

<style>
button{
	margin: 5px;
}
</style>
