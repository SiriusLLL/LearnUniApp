<template>
	<view class="out">
		<view class="box" v-for="(item,index) in 10">box模块{{index + 1}}</view>
		<view v-for="item in nba">
			球星：{{item.name}} - 号码：{{item.num}}
		</view>
	</view>
</template>

<script setup>
	import {
		ref
	} from "vue";
	const nba = ref([{
		name: "乔丹",
		num: 23
	}, {
		name: "詹姆斯",
		num: 6
	}, {
		name: "科比",
		num: 24
	}])
</script>

<style lang="scss" scoped>

</style>