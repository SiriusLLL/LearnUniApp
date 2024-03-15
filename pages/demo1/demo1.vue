<template>
	<view>
		<swiper indicator-dots indicator-color="rgba(255,255,255,0.3)" indicator-active-color="#fff" circular=""
			autoplay="" interval="2000">
			<swiper-item>
				<image src="../../static/hc.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/wxr.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/haha.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/xixi.png" mode="aspectFill"></image>
			</swiper-item>
			<swiper-item>
				<image src="../../static/daxiao.png" mode="aspectFill"></image>
			</swiper-item>
		</swiper>
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

<style lang="scss">
	swiper {
		width: 100vw;
		height: 200px;
		border: 1px solid green;

		swiper-item {
			width: 100%;
			height: 100%;
			background-color: pink;
		}

		swiper-item:nth-child(2n) {
			background-color: orange;
		}
	}

	.pic1 {
		width: 100px;
		height: 100px;
	}
</style>