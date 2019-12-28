<template>
  <div class="account-page">
	 <view class="tool_ui">
	 	<div @click="scanCoder"  class="scan-icon left" id="scancodes"></div>
	 </view>
	  <view class="account_page_header">
	  	<view class="">
	  		登录网易云音乐
	  	</view>
		<view class="">
			手机电脑多端同步，尽享海量高品质音乐
		</view>
		<view  class="loginnow" id="login">
			<span>立即登录</span>
		</view>
	  </view>
	  <view class="banner">
		  <view class="item">
			  <view>开通黑胶VIP</view>
			  <view>新客仅5元 <uni-icons type="arrowright" size="20" color="#eee"></uni-icons></view>
		  </view>
		  <view class="item">
			 <view>会员中心</view>
			 <view>去装扮圣诞头像吧<uni-icons type="arrowright" size="20" color="#eee"></uni-icons></view>
		  </view>
	  </view>
	  <view class="category_fn_link">
	  	 <view class="item">
			 <uni-icons type="email" size="30" class="uni-icon" color="#f10215"></uni-icons>
			 <view><span>消息</span></view>
		 </view>
	  	 <view class="item">
			 <img :src="imgs.shop" mode=""/>
			 <view>
				 <span>商城</span>
				 <span  class="last">圣诞5折献礼</span>
			</view>
		 </view>
		 <view class="item">
			 <img :src="imgs.show" alt="">
			  <view>
				  <span>演出</span>
				  <span  class="last">夜宴乐队</span>
			  </view>
			 
		 </view>
		 <view class="item">
		 	  <img :src="imgs.ge" alt="">
		 	 <view><span>个性装扮</span></view>
		 </view>
	  
	  </view>
	  <uni-list class="first uni-list-parent">
	      <uni-list-item title="口袋彩铃"  :thumb="imgs.cai" :show-arrow="true"></uni-list-item>
	      <uni-list-item title="我的订单" :thumb="imgs.order"></uni-list-item>
	  </uni-list>
	  <uni-list class="second uni-list-parent">
	      <uni-list-item title="设置"  :thumb="imgs.setting" :show-arrow="true"></uni-list-item>
	      <uni-list-item title="夜间模式" :thumb="imgs.ye" :show-switch="true" :show-arrow="true" ></uni-list-item>
	  	  <uni-list-item title="定时关闭" :thumb="imgs.dingtime"></uni-list-item>
		  <uni-list-item title="音乐闹钟" :thumb="imgs.nao"></uni-list-item>
	  </uni-list>
	  <uni-list class="third uni-list-parent">
	      <uni-list-item title="在线听歌免流量" :thumb="imgs.online" :show-arrow="true"></uni-list-item>
	      <uni-list-item title="优惠券" :thumb="imgs.you"  :show-arrow="true" ></uni-list-item>
	  		  <uni-list-item title="青少年模式"  :thumb="imgs.qing" style="position: relative;">
				  <view class="note" style="float: right;position: absolute;right: 50px;">
				  	未开启
				  </view>
			  </uni-list-item>
	  </uni-list>

	  <uni-list class="fourth uni-list-parent">
	  		  <uni-list-item title="分享网易云音乐" :thumb="imgs.fen" :show-arrow="true"></uni-list-item>
	  		  <uni-list-item title="关于" :thumb="imgs.about"  :show-arrow="true" ></uni-list-item>
	  </uni-list>
  </div>
</template>

<script>
	import uniList from "@/components/uni-list/uni-list.vue"
	import uniListItem from "@/components/uni-list-item/uni-list-item.vue"
	import uniIcons from "@/components/uni-icons/uni-icons.vue"
	import cai from "./imgs/cailine.png"
	import order from "./imgs/order.png"
	import setting from "./imgs/setting.png"
	import ye from "./imgs/ye.png"
	import fen from "./imgs/fen.png"
	import about from "./imgs/about.png"
	import dingtime from "./imgs/dingtime.png"
	import nao from "./imgs/nao.png"
	import online from "./imgs/online.png"
	import you from "./imgs/you.png"
	import qing from "./imgs/bao.png"
	import shop from "./imgs/shop.png"
	import show from "./imgs/show.png"
	import ge from "./imgs/ge.png"
export default {
	data(){
		return {
			imgs:{
				cai,
				order,
				setting,
				ye,
				about,
				fen,
				dingtime,
				nao,
				online,
				you,
				qing,
				shop,
				show,
				ge
			}
		}
	},
	methods:{
	scanCoder:function(){
		// #ifdef APP-PLUS
		let ids=plus.barcode.getBarcodeById("scancodes");
		let scaner=plus.barcode.create({
			'id':ids,
		})
		// #endif 
	   },
	   login(){
		   console.log('登录')
	   }
	},
	components: {uniList,uniListItem,uniIcons},
	onLoad:function(){
		// #ifdef MP-WEIXIN
		var jweixin = require('jweixin-module')  
		jweixin.ready(function(){  
		    // TODO  
		});
		// #endif
	}
};
</script>

<style lang="less" scoped>
	.account-page{
		background: #f5f5f5;
		padding-top: 25px;
	}
	.tool_ui{
		display: flex;
		flex-wrap: nowrap;
		align-items: center;
		height: 40px;
		position: relative;
		z-index: 111;
		width: 100%;
		padding: 13px;
		background: #fff;
		.scan-icon{
			width: 40px;

			height: 40px;
			background: url("./imgs/scan.png") no-repeat;
			background-size: 100% 100%;
			margin: 10px 0;
		}
	}
	.account_page_header{
		font-size: 13px;
		text-align: center;
		line-height: 30px;
		width: 100%;
		overflow: hidden;
		padding-top: 10px;
		background: #fff;
		.loginnow{
			border-radius: 15px;
			width: 90%;
			height: 35px;
			border: 1px solid #ccc;
			margin: auto;
			margin-top: 10px;
			display: flex;
			align-items: center;
			justify-content: center;

		}
	}
	.banner{
		width: 90%;
		border-radius: 8px 8px 0 0;
		background: #000000;
		display: flex;
		flex-wrap: nowrap;
		align-items: center;
		height: 45px;
		margin-left: auto;
		margin-right: auto;
		margin-top: 20px;
		padding: 5px 0;
		.item{
			color: #F3F3F3;
			height: 100%;
			width: 45%;
			text-align: center;
			display: flex;
			flex-wrap: wrap;
			align-items: center;
			text-align: left;
			view{
				font-size: 10px;
				text-align: center;
				padding-left: 25px;
			}
		}
	}
	.category_fn_link{
		margin: 5px 0;
		width: 100%;
		height: 80px;
		display: flex;
		flex-wrap: nowrap;
		margin: 0 auto;
		padding-top: 10px;
		background: #fff;
		.item{
			text-align: center;
			display: flex;
			flex-wrap: wrap;
			width: 25%;
			height: 100%;
			font-size: 12px;
			color: #000;
			text-align: center;
			.uni-icon{
				width: 100%;
				text-align: center;
			}
			img{
				width: 30px;
				height: 25px;
				color: #f10215;
				margin: auto;
				text-align: center;
			}
			view{
				color: #000000;
				width: 100px;
				margin-top: 5px;
				padding-bottom: 12px;
				span{
					display: block;
					vertical-align: top;
					&.last{
					color: #ccc;
					}
				}
				
			}
		}
	}
	.uni-list-parent{
		margin: 10px 0;
		width: 100%;
		background: #fff;
	}
</style>
