<template>
	<view>
		<view class="itemStyle active" v-for="(item, index) in itemList" :key="index" @tap="openWin(item.path)" :style="item.style||''">
			<view>{{item.name}}</view>
			<uni-icons type="arrowright" color="#999999" :size="30"/>
		</view>
	</view>
</template>

<script>
	import uniIcons from './QS-inputs-split/uniIcons/uni-icons.vue';
	export default {
		components: { uniIcons },
		props: {
			itemList: {
				type: Array,
				default() {
					return [];
				}
			}
		},
		methods: {
			openWin(path) {
				uni.navigateTo({
					url: path
				})
			}
		}
	}
</script>

<style>
</style>
