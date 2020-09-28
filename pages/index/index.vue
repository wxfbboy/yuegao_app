<template>
	<view class="index-body">
		<u-navbar title="" :background="background" title-color="#ffffff" back-icon-color="#ffffff" :is-back="false">
			<view class="slot-wrap">
				<view class="input-box">
					<input class="uni-input search-input" placeholder="搜索关键字" />
					<u-icon name="search" class="search-icon"></u-icon>
				</view>
			</view>
		</u-navbar>
		<view class="swiper-wrap">
			<view class="swiper-box">
				<swiper class="swiper" indicator-dots="true" interval="interval" duration="500" autoplay="true">
					<swiper-item v-for="(item,index) in swiperData" :key="index">
						<view class="swiper-item uni-bg-red">
							<image :src="item.image" class="swiper-image"></image>
						</view>
					</swiper-item>
				</swiper>
			</view>
		</view>
		<view class="categories">
			<u-grid :col="3" :border="gridBorder">
				<u-grid-item>
					<image src="/static/gufeng.jpg" class="categoires-icon"></image>
					<view class="grid-text">古风</view>
				</u-grid-item>
				<u-grid-item>
					<image src="/static/rihan.jpg" class="categoires-icon"></image>
					<view class="grid-text">日韩</view>
				</u-grid-item>
				<u-grid-item>
					<image src="/static/xieshi.jpg" class="categoires-icon"></image>
					<view class="grid-text">写实</view>
				</u-grid-item>
			</u-grid>
		</view>
		<view class="promotion">
			<view class="title">推荐专区</view>
			<view class="product-list">
				<view class="product">
					<image src="/static/rihan.jpg" class="product-image"></image>
					<view class="product-name">日韩头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
				<view class="product">
					<image src="/static/xieshi.jpg" class="product-image"></image>
					<view class="product-name">古风头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
				<view class="product">
					<image src="/static/rihan.jpg" class="product-image"></image>
					<view class="product-name">日韩头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
				<view class="product">
					<image src="/static/xieshi.jpg" class="product-image"></image>
					<view class="product-name">古风头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
				<view class="product">
					<image src="/static/rihan.jpg" class="product-image"></image>
					<view class="product-name">日韩头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
				<view class="product">
					<image src="/static/xieshi.jpg" class="product-image"></image>
					<view class="product-name">古风头像定制</view>
					<view class="product-info">
						<view class="price">￥100</view>
						<view class="slogan">12人付款</view>
					</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				swiperData: [{
						id: 1,
						image: '/static/1.jpg'
					},
					{
						id: 2,
						image: '/static/2.jpg'
					},
				],
				background: {
					backgroundColor: '#ffffff',
					boxShadow: '0upx 8upx 25upx rgba(0, 0, 0, 0.2)'
				},
				gridBorder: false
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style lang="scss">
	.index-body {
		// background-color: #eee;
		.swiper-wrap {
			padding: 30rpx;
			border-radius: 20%;
			.swiper-box {
				border-radius: 15upx;
				overflow: hidden;
				box-shadow: 0upx 8upx 25upx rgba(0, 0, 0, 0.2);
				.swiper-item{
					.swiper-image{
						width: 100%;
						// height: 100%;
					}
				}
			}
		}

		.categories {
			margin: 5upx auto;
			.categoires-icon {
				width: 150upx;
				height: 150upx;
				border-radius: 50%;
				box-shadow: 0upx 8upx 25upx rgba(0, 0, 0, 0.2);
			}

			.grid-text {
				padding-top: 20upx;
			}
		}
		
		.promotion{
			width: 100%;
			text-align: left;
			padding-top: 10upx;
			.title{
				font-size: 32upx;
				font-weight: 1000;
				padding-left: 40upx;
				padding-top: 6upx;
				padding-bottom: 6upx;
				margin-bottom: 20upx;
			}
			.product-list{
				width: 100%;
				padding:0 5% 1vw 5%;
				display: flex;
				justify-content:space-between;
				flex-wrap: wrap;
				.product{
					width: 320upx;
					box-shadow: 0upx 8upx 25upx rgba(0, 0, 0, 0.2);
					overflow: hidden;
					border-radius: 15upx;
					margin-bottom: 25upx;
					.product-image{	
						width: 320upx;
						height: 320upx;
						word-wrap: break-word;
					}
					.product-name{
						display: inline-block;
						height: 90upx;
						overflow: hidden;
						text-overflow:ellipsis;
						padding: 10upx 15upx;
						font-weight: 600;
					}
					.product-info{
						display: flex;
						justify-content: space-between;
						padding: 15upx;
						.price{
						    color: #e65339;
						    font-size: 30upx;
						    font-weight: 600;
						}
						.slogan{
							color: #807c87;
						    font-size: 20upx;
						}
					}
				}
			}
		}

		.slot-wrap {
			width: 100%;
			display: flex;
			justify-content: center;
			padding: 0 60upx;

			.input-box {
				width: 100%;
				height: 25px;
				background-color: #f5f5f5;
				border-radius: 25upx;
				position: relative;

				input {
					padding-left: 28upx;
					height: 25px;
					font-size: 28upx;
				}

				.search-icon {
					position: absolute;
					top: 0;
					bottom: 0;
					right: 0;
					margin-right: 10px;
				}
			}
		}
	}
</style>
