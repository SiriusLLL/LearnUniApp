<template>
	<view>
		<image :src="picUrl" mode=""></image>
		<button type="primary" :loading="false" :disabled="true">按钮</button>
	</view>
	<view class="box" :class="{active:isActive}">v-bind指令</view>

	<view class="box" :class="isActive?'active' : ''"></view>

	<view class="box" :style="{width:'300px',height:260+'px',fontSize:size+'px'}">内联样式</view>
</template>

<script setup>
	import {
		ref
	} from "vue";

	const isActive = ref(false);
	const size = ref(30)
	const arrs = ref(["../../static/hc.png", "../../static/haha.png", "../../static/wxr.png", "../../static/xixi.png"]);
	const picUrl = ref("../../static/hc.png");

	let i = 0;
	setInterval(() => {
		i++;
		picUrl.value = arrs.value[i % 4];
		isActive.value = !isActive.value;
		// size.value += i;
	}, 1000);
</script>

<style lang="scss">
	.box {
		width: 200px;
		height: 200px;
		background: orange;
		font-size: 20px;
	}

	.active {
		background: #fff;
	}
</style>