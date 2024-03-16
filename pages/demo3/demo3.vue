<template>
	<view>
		<image :src="picUrl" mode=""></image>
		<button type="primary" :loading="false" :disabled="true">按钮</button>
	</view>
</template>

<script setup>
	import {
		ref
	} from "vue";

	const arrs = ref(["../../static/hc.png", "../../static/haha.png", "../../static/wxr.png", "../../static/xixi.png"]);
	const picUrl = ref("../../static/hc.png");

	let i = 0;
	setInterval(() => {
		i++;
		picUrl.value = arrs.value[i % 4];
	}, 1000)
</script>

<style>

</style>