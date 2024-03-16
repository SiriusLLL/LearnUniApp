<template>
	<view class="box" @click="onClick">
		{{num}}
	</view>

	<switch @change="onChange"></switch>
	<button type="primary" :disabled="isDisabled"> 普通按钮</button>
</template>

<script setup>
	import {
		ref
	} from "vue";
	const num = ref(1);
	const isDisabled = ref(false);

	function onClick() {
		num.value++;
	}

	function onChange(e) {
		isDisabled.value = e.detail.value;
		// console.log(e.detail.value);
	}
</script>

<style lang="scss">
	.box {
		width: 200px;
		height: 200px;
		background: orange;
	}
</style>