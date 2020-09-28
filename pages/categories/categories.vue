<template>
	<view>
		<u-navbar title="" :background="background" title-color="#ffffff" back-icon-color="#ffffff" :is-back="false">
			<view class="slot-wrap">
				<view class="input-box">
					<input class="uni-input search-input" placeholder="搜索关键字" />
					<u-icon name="search" class="search-icon"></u-icon>
				</view>
			</view>
		</u-navbar>
		<view class="categories-content">
			<scroll-view  scroll-y="true" class="categories-left" >
				<view class="links">
					<view class="active">
						<view class="block"></view>
						<text>古风</text>
					</view>
					<view>
						<view class="block"></view>
						<text>日韩</text>
					</view>
					<view>
						<view class="block"></view>
						<text>写实</text>
					</view>
				</view>
			</scroll-view>
			<scroll-view  scroll-y="true" class="categories-right" >
				<u-grid :col="3">
					<u-grid-item>
						<image src="/static/gufeng.jpg" class="icon"></image>
						<view class="grid-text">头像</view>
					</u-grid-item>
					<u-grid-item>
						<image src="/static/gufengbanshen.jpg" class="icon"></image>
						<view class="grid-text">半身</view>
					</u-grid-item>
					<u-grid-item>
						<image src="/static/gufengquanshen.jpg" class="icon"></image>
						<view class="grid-text">全身</view>
					</u-grid-item>
					<u-grid-item>
						<image src="/static/gufengbeijing.jpg" class="icon"></image>
						<view class="grid-text">背景</view>
					</u-grid-item>
				</u-grid>
			</scroll-view>
		</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				background: {
					backgroundColor: '#ffffff',
					// boxShadow: '0upx 8upx 25upx rgba(0, 0, 0, 0.2)'
				},
			};
		}
	}
</script>

<style lang="scss">
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
	.categories-content{
		display: flex;
		position: fixed;
		width: 100%;
		height: 100%;
		.categories-left,.categories-right{
			height: 100%;
		}
		.categories-left{
			width: 25%;
			left: 0upx;
			background-color: #f2f2f2;
			.links{
				view{
					// display: block;
					height: 90upx;
					line-height: 90upx;
					text-align: center;
					font-size: 24upx;
					position: relative;
					.block{
						position: absolute;
						left: 0;
					}
					&.active{
						background-color:#fff;
						// border-bottom: 1px #e0e0e0 solid;
						// border-right: 1px #e0e0e0 solid;	
						.block{
							position: absolute;
							left: 0;
							background-color: #f06c7a;
							width: 8upx;
						}
					}
				}
			}
		}
		.categories-right{
			width: 75%;
			right: 0upx;
			.icon {
				width: 100upx;
				height: 100upx;
				border-radius: 50%;
				box-shadow: 0upx 8upx 25upx rgba(0, 0, 0, 0.2);
			}
			// background-color: #F0AD4E;
		}
	}
</style>
