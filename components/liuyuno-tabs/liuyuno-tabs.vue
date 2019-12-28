<template>
	<view class="tab-box" v-if="tabList.length > 0">
		<view class="horizontal">
			<scroll-view :scroll-x="true" style="white-space: nowrap; display: flex" scroll-with-animation :scroll-left="slider.scrollLeft">
				<block v-for="(item, index) in tabList" :key="index" >
				<view class="item" :class="{ active: activeIndex === index }" :id="'tab_'+index" @click="tabClick(index)">{{ item.text || item }}</view>
				</block>
				<view class="underline" :style="'transform:translateX(' + slider.left + 'px);width:' + slider.width + 'px'"></view>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		name: 'liuyuno-tabs',
		props: {
			tabData: {
				type: Array,
				default: () => []
			},
			defaultIndex: {
				type: Number,
				default: 0
			},
			underLinePadding: {
				type: Number,
				default: 10
			},
		},
		data() {
			return {
				tabList: [],
				slider: {
					left: 0,
					width: 0,
					scrollLeft: 0
				},
				activeIndex: 0
			};
		},
		watch: {
			tabData(value) {
				this.tabList = value;
				setTimeout(() => {
					this.updateTabWidth();
				}, 0);
			},
		},
		mounted() {
			this.tabList = this.tabData;
			this.activeIndex = this.defaultIndex;
			
			setTimeout(() => {
				this.updateTabWidth();
			}, 0);
		},
		methods: {
			updateTabWidth(index = 0) {
				let data = this.tabList;
				
				if (data.length == 0) return false;
				
				const query = uni.createSelectorQuery().in(this);
				
				query.select('#tab_' + index).boundingClientRect((res) => {
					data[index]._slider = {
						width: res.width,
						left: res.left,
						scrollLeft: res.left - (data[index - 1] ? data[index - 1]._slider.width : 0),
					};

					if (this.activeIndex == index) {
						this.tabToIndex(this.activeIndex);
					}

					index++;
					if (data.length > index) {
						this.updateTabWidth(index);
					}
				}).exec();
			},
	
			tabToIndex(index) {

				let _slider = this.tabList[index]._slider;
	
				this.slider = {
					left: _slider.left + this.underLinePadding,
					width: _slider.width - this.underLinePadding * 2,
					scrollLeft: _slider.scrollLeft,
				}
				// this.slider = _slider;
			},
			
			tabClick(index) {
				this.activeIndex = index;
				this.tabToIndex(index);
				this.$emit('tabClick', index);
			}
		}
	}
</script>

<style lang="less">
	.tab-box {
		width: 100vw;
		color: rgba(0, 0, 0, 0.8);
		display: flex;
		height: 90upx;
		background: #fff;
		font-size: 28upx;
		box-shadow: 0 1px 5px rgba(0, 0, 0, 0.06);
		position: relative;
		z-index: 10;
		.active {
			color: #e54d42;
		}
		.horizontal {
			width: 100%;
			.item { 
				height: 84upx; 
				display: inline-block;
				line-height: 90upx;
				text-align: center;
				padding: 0 30upx;
			}
			.underline {
				height: 4upx;
				background-color: #e54d42;
				border-radius: 3px;
				transition: .5s;
			}
		}
	}
</style>
