<template>
	<view class="out">
		<!-- <input type="text" :value="iptValue" @focus="onFocus" @blur="onBlur" /> -->
		<input type="text" :value="iptValue" @focus="isActive=true" @blur="isActive=false" />
		<image src="../../static/chicken.gif" mode="" class="pic" :class="isActive ? 'active':''"></image>
	</view>
</template>

<script setup>
	import {
		ref
	} from "vue";
	const iptValue = ref("");
	const isActive = ref(false);

	// function onFocus(e) {
	// 	isActive.value = true;
	// }

	// function onBlur(e) {
	// 	isActive.value = false;
	// }
</script>

<style lang="scss" scoped>
	.out {
		padding: 0 20px;
		margin-top: 40px;
		position: relative;

		input {
			border: 1px solid #ccc;
			position: relative;
			z-index: 2;
			background: #fff;
			padding: 0 10px;
		}

		.pic {
			width: 24px;
			height: 24px;
			z-index: 1;
			position: absolute;
			top: 0px;
			left: calc(50% - 12px);
			transition: top 0.3s;
		}

		.pic.active {
			top: -24px;
		}
	}
</style>