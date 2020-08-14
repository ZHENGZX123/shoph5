<template>
	<div style="margin-bottom: 100px;display: flex;flex-direction: column;justify-content: center;">
		<div class="home-title">
			<img style="width:1.5rem;height: 0.24rem;" src="../../assets/huayu/huayu.png" />
			<img style="width: 2.16rem;height: 0.335rem;margin-top: 0.3rem;margin-right: 10px;" src="../../assets/huayu/huayu2.png" />
		</div>
		<img style="width: 100%;7.79rem" src="../../assets/huayu/banner-bg.jpg" />

		<div class="title-line">
			<img class="title-icon" src="../../assets/huayu/left-icon.png" />
			<div style="flex-shrink: 0;">新品上市</div>
			<img class="title-icon" src="../../assets/huayu/right-icon.png" />
		</div>

		<img v-if="purchaseList.length>=0" class="new-img" :src="purchaseList[0].pic" @click="goUrl(purchaseList[0].wap_url)" />

		<div class="title-line">
			<img class="title-icon" src="../../assets/huayu/left-icon.png" />
			<div style="flex-shrink: 0;">限时秒杀</div>
			<img class="title-icon" src="../../assets/huayu/right-icon.png" />
		</div>
		<div class="flexrow box-line flexac" style="width: 90%;padding: 10px;margin: 5px auto;" v-for="(item ,index) in purchaseList">
			<img class="box-item-img" src="../../assets/images/assemble.jpg" />
			<div class="flexcolumn" style="margin-left: 20px;width: 100%;justify-content: space-between;">
				<div class="shop-title">混合坚果灌装礼盒</div>
				<div class="shop-price">原价：¥238</div>
				<div class="flexrow" style="align-items:flex-end;justify-content: space-between;width: 100%;">
					<div class="shop-price2">199
						<img style="width: 10px;height: 10px;margin-left: -5px;" src="../../assets/huayu/love.png"></img>
					</div>
					<div class="buy">立即抢购</div>
				</div>
			</div>
		</div>
		<div class="flexcolumn flexjc " style="width: 100%" v-for="(item ,index) in purchaseList">
			<div class="title-line">
				<img class="title-icon" src="../../assets/huayu/left-icon.png" />
				<div style="flex-shrink: 0;">人气好物</div>
				<img class="title-icon" src="../../assets/huayu/right-icon.png" />
			</div>
			<img class="new-img" src="../../assets/huayu/banner-bg.jpg" />
			<div class="flexrow " style="flex-wrap: wrap;width: 94%;margin: 0 auto;">
				<div style="width:50%;">
					<div class="flexcolumn box-line" style="margin: 10px;padding: 0.11rem;background: #F7F7F7;">
						<img class="box-item-img2" src="../../assets/images/assemble.jpg" />
						<div class="shop-title" style="font-size: 0.32rem;margin-top: 7px;">混合坚果灌装礼盒</div>
						<div class="shop-price" style="font-size:0.01rem ;margin-top: 2px;">原价：¥238</div>
						<div class="flexrow" style="align-items:flex-end;justify-content: space-between;width: 100%;margin-top: 5px;">
							<div class="flexrow  shop-price2" style="font-size: 0.5rem;align-items:flex-end;">199
								<img style="width: 8px;height: 8px;margin-bottom: 7px;" src="../../assets/huayu/love.png"></img>
							</div>
							<div class="buy2">立即抢购</div>
						</div>
					</div>
				</div>
				<div style="width:50%;">
					<div class="flexcolumn box-line" style="margin: 10px;padding: 0.11rem;background: #F7F7F7;">
						<img class="box-item-img2" src="../../assets/images/assemble.jpg" />
						<div class="shop-title" style="font-size: 0.32rem;margin-top: 7px;">混合坚果灌装礼盒</div>
						<div class="shop-price" style="font-size:0.01rem ;margin-top: 2px;">原价：¥238</div>
						<div class="flexrow" style="align-items:flex-end;justify-content: space-between;width: 100%;margin-top: 5px;">
							<div class="flexrow  shop-price2" style="font-size: 0.5rem;align-items:flex-end;">199
								<img style="width: 8px;height: 8px;margin-bottom: 7px;" src="../../assets/huayu/love.png"></img>
							</div>
							<div class="buy2">立即抢购</div>
						</div>
					</div>
				</div>
				<div style="width:50%;">
					<div class="flexcolumn box-line" style="margin: 10px;padding: 0.11rem;background: #F7F7F7;">
						<img class="box-item-img2" src="../../assets/images/assemble.jpg" />
						<div class="shop-title" style="font-size: 0.32rem;margin-top: 7px;">混合坚果灌装礼盒</div>
						<div class="shop-price" style="font-size:0.01rem ;margin-top: 2px;">原价：¥238</div>
						<div class="flexrow" style="align-items:flex-end;justify-content: space-between;width: 100%;margin-top: 5px;">
							<div class="flexrow  shop-price2" style="font-size: 0.5rem;align-items:flex-end;">199
								<img style="width: 8px;height: 8px;margin-bottom: 7px;" src="../../assets/huayu/love.png"></img>
							</div>
							<div class="buy2">立即抢购</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div class="flex flexrow" style="justify-content: space-around;width: 92%;margin: 10px auto;">
			<div class="flex flexcolumn box-line more-item flexac">
				<div>购物须知</div>
				<div style="margin-top: 4px;font-size: 0.2rem;font-weight: 400;">点击了解更多>></div>
			</div>
			<div class="flex flexcolumn box-line more-item flexac">
				<div>证照公示</div>
				<div style="margin-top: 4px;font-size: 0.2rem;font-weight: 400;">点击了解更多>></div>
			</div>
		</div>
		<div class="flex flexcolumn box-line" style="padding: 7px; width: 85%;margin: 10px auto;">
			<div class="flexrow flexac card-item" style="margin-top: 10px;" v-for="(item, index) in cardList" @click="goUrl(item.url)">
				<img style="width: 3.22rem;height: 2.22rem;" v-bind:src="item.imageUrl" />
				<div class="flexcolumn" style="margin-left: 10px;">
					<div>{{item.title}}</div>
					<div class="card-bt-item">点击在线办理</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import {
		getHomeData,
	} from "@api/public";
	import cookie from "@utils/store/cookie";
	import {
		getSeckillConfig,
		getSeckillList
	} from "@api/activity";
	import {
		isWeixin
	} from "@utils/index";
	import {
		openShareAll,
		wxShowLocation
	} from "@libs/wechat";
	import {
		goShopDetail
	} from "@libs/order";
	const MAPKEY = "mapKey";
	const HAS_COUPON_WINDOW = "has_coupon_window";
	const LONGITUDE = "user_longitude";
	const LATITUDE = "user_latitude";
	export default {
		data: function() {
			return {
				purchaseList: [{}, {}, {}],
				classificationList: [{}, {}, {}],
				cardList: [{
					imageUrl: require('../../assets/huayu/card1.png'),
					title: '工银女性行用卡光芒系列Plus版 ',
					url: 'https://elife.icbc.com.cn/OFSTCARD/creditCard/apply.do?channel=109HSXFHSXF000100000000000&paraPromoCode=EW888001091661HSXF1&coreCode=HZDW000070462 '
				}, {
					imageUrl: require('../../assets/huayu/card2.png'),
					title: '工银微信信用卡',
					url: 'https://elife.icbc.com.cn/OFSTCARD/creditCard/apply.do?channel=109HSXFHSXF000100000000000&paraPromoCode=EW888001091661HSXF1&coreCode=HZDW000046964'
				}, {
					imageUrl: require('../../assets/huayu/card3.png'),
					title: '工银长隆卡',
					url: 'https://elife.icbc.com.cn/OFSTCARD/creditCard/apply.do?channel=109HSXFHSXF000100000000000&paraPromoCode=EW888001091661HSXF1&coreCode=HZDW000002961 '
				}]
			};
		},
	
		
		mounted: function() {
			let that = this;
			getHomeData().then(res => {
				that.mapKey = res.data.tengxun_map_key;
				cookie.set(MAPKEY, that.mapKey);
				that.$set(that, "purchaseList", res.data.banner);
				that.subscribe = res.data.subscribe;
				if (!that.subscribe && that.followUrl) {
					setTimeout(function() {
						that.followHid = true;
					}, 200);
				} else {
					that.followHid = false;
				}
				if (res.data.site_name) document.title = res.data.site_name;
				this.showCoupon = !cookie.has(HAS_COUPON_WINDOW) &&
					res.data.couponList.some(coupon => coupon.is_use);
				if (!cookie.get(LATITUDE) && !cookie.get(LONGITUDE)) this.getWXLocation();
			});
		
			getSeckillConfig().then(res => {
						  console.log(res)
			  // that.$set(that, "timeList", res.data.seckillTime);
			  // that.$set(that, "active", res.data.seckillTimeIndex);
			  // that.datatime = that.timeList[that.active].stop;
			  // that.loadingList = false;
			  // that.getSeckillList();
			
			});
		},

		methods: {
			
			
			getSeckillList: function() {
			  var that = this;
			  var time = that.timeList[that.active].id;
			  getSeckillList(time, { page: that.page, limit: that.limit })
			    .then(res => {
			      that.status = res.data.length < that.limit;
			      that.seckillList.push.apply(that.seckillList, res.data);
			      that.page++;
			      that.loadingList = false;
			    })
			    .catch(() => {
			      that.loadingList = false;
			    });
			},
			
			goUrl(url) {

				let newStr = url.indexOf("http") === 0;
				if (newStr) {
					window.location.href = url;
				} else {
					this.$router.push({
						path: url
					});
				}
			},

			getWXLocation() {
				if (isWeixin()) {
					wxShowLocation();
				} else {
					if (!this.mapKey)
						console.log("暂无法使用查看地图，请配置您的腾讯地图key");
					let loc;
					// if (_this.$route.params.mapKey) _this.locationShow = true;
					//监听定位组件的message事件
					window.addEventListener(
						"message",
						function(event) {
							loc = event.data; // 接收位置信息 LONGITUDE
							console.log("location", loc);
							if (loc && loc.module == "geolocation") {
								cookie.set(LATITUDE, loc.lat);
								cookie.set(LONGITUDE, loc.lng);
							} else {
								cookie.remove(LATITUDE);
								cookie.remove(LONGITUDE);
								//定位组件在定位失败后，也会触发message, event.data为null
								console.log("定位失败");
							}
						},
						false
					);
				}
			},
		}
	};
</script>
<style>
	.home-title {
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		margin-top: 0.38rem;
		margin-bottom: 10px;
		padding-left: 0.47rem;
	}

	.title-line {
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
		font-size: 0.4rem;
		font-family: PingFang SC;
		font-weight: bold;
		color: rgba(0, 127, 118, 1);
		margin-top: 0.3rem;
		margin-bottom: 0.3rem;
	}

	.title-icon {
		width: 1.125rem;
		height: 0.175rem;
		margin-left: 10px;
		margin-right: 10px;
	}

	.new-img {
		width: 90%;
		height: 2.66rem;
		border-radius: 10px;
		border: 4px solid rgba(0, 127, 117, 1);
		margin: 0 auto;
		text-align: center;
	}

	.box-line {
		border-radius: 10px;
		border: 2px solid rgba(0, 127, 117, 1);
	}

	.flexrow {
		display: flex;
		flex-direction: row;
	}

	.flexcolumn {
		display: flex;
		flex-direction: column;
	}

	.flexjc {
		justify-content: center;
	}

	.flexac {
		align-items: center;
	}

	.box-item-img {
		width: 2rem;
		height: 2rem;
		border-radius: 10px;
	}

	.box-item-img2 {
		width: 2.8rem;
		height: 2.8rem;
		padding: 0.2rem;
		margin: 0 auto;
		background-color: #FFFFFF;
		border-radius: 10px;
	}

	.shop-title {
		font-size: 0.35rem;
		font-family: PingFang SC;
		font-weight: bold;
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
		color: rgba(2, 0, 0, 1);
	}

	.shop-price {
		font-size: 0.25rem;
		font-family: PingFang SC;
		font-weight: 500;
		text-decoration: line-through;
		margin-top: 7px;
		color: rgba(102, 102, 102, 1);
	}

	.shop-price2 {
		font-size: 0.64rem;
		font-family: NumberOnly;
		font-weight: bold;
		color: rgba(229, 25, 20, 1)
	}

	.buy {
		background: rgba(229, 25, 21, 1);
		border-radius: 20px;
		font-size: 0.3rem;
		font-family: PingFang SC;
		font-weight: 500;
		padding: 8px 15px;
		margin-bottom: 5px;
		color: rgba(255, 255, 255, 1);
	}

	.buy2 {
		background: rgba(229, 25, 21, 1);
		border-radius: 20px;
		font-size: 0.2rem;
		font-family: PingFang SC;
		font-weight: 500;
		padding: 5px 10px;
		flex-shrink: 0;
		margin-bottom: 5px;
		color: rgba(255, 255, 255, 1);
	}

	.more-item {
		width: 45%;
		padding: 10px;
		font-size: 0.35rem;
		font-family: PingFang SC;
		font-weight: bold;
		color: rgba(255, 0, 0, 1);
	}

	.card-item {
		font-size: 0.18rem;
		font-family: PingFang SC;
		font-weight: bold;
		color: rgba(2, 0, 0, 1);
	}

	.card-bt-item {
		width: 2rem;
		background: rgba(229, 25, 21, 1);
		font-size: 0.24rem;
		font-family: PingFang SC;
		font-weight: bold;
		border-radius: 20px;
		margin-top: 15px;
		padding: 3px 5px;
		text-align: center;
		color: rgba(252, 252, 252, 1);
	}

	body {
		background-color: #F7F7F7;
	}
</style>
