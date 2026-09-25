<template>
	<view class="content">
		<view class="maxPhoto" v-show="isShow" @click="isShow = false">
			<image :src="src" mode="widthFix" @click="isShow = true; src = item"></image>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box1.h}}</view>
				<view>{{box1.time}}</view>
				<view>{{box1.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box1.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(1)">复制文案</view>
				<view @click="downloadMedia(box1.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box2.h}}</view>
				<view>{{box2.time}}</view>
				<view>{{box2.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box2.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(2)">复制文案</view>
				<view @click="downloadMedia(box2.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box3.h}}</view>
				<view>{{box3.time}}</view>
				<view>{{box3.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box3.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(3)">复制文案</view>
				<view @click="downloadMedia(box3.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box4.h}}</view>
				<view>{{box4.time}}</view>
				<view>{{box4.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box4.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(4)">复制文案</view>
				<view @click="downloadMedia(box4.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box5.h}}</view>
				<view>{{box5.time}}</view>
				<view>{{box5.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box5.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(5)">复制文案</view>
				<view @click="downloadMedia(box5.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box6.h}}</view>
				<view>{{box6.time}}</view>
				<view>{{box6.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box6.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(6)">复制文案</view>
				<view @click="downloadMedia(box6.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box7.h}}</view>
				<view>{{box7.time}}</view>
				<view>{{box7.text}}</view>
			</view>
			<view class="box-c">
				<video src="https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/2.mp4" controls></video>
			</view>
			<view class="box-b">
				<view @click="copyText(7)">复制文案</view>
				<view @click="downloadMedia(box7.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box8.h}}</view>
				<view>{{box8.time}}</view>
				<view>{{box8.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box8.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(8)">复制文案</view>
				<view @click="downloadMedia(box8.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box9.h}}</view>
				<view>{{box9.time}}</view>
				<view>{{box9.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box9.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(9)">复制文案</view>
				<view @click="downloadMedia(box9.image)">下载图文</view>
			</view>
		</view>
		<view class="box">
			<view class="box-t">
				<view>{{box10.h}}</view>
				<view>{{box10.time}}</view>
				<view>{{box10.text}}</view>
			</view>
			<view class="box-c">
				<image v-for="item in box10.image" :src="item" mode="" @click="isShow = true; src = item"></image>
			</view>
			<view class="box-b">
				<view @click="copyText(10)">复制文案</view>
				<view @click="downloadMedia(box10.image)">下载图文</view>
			</view>
		</view>
	</view>
</template>

<script>
	import {
		Static
	} from "vue";

	export default {

		data() {
			return {
				isShow: false,
				src: "https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281039002.jpg",
				box1: {
					h: "美加优选最新上线",
					time: "2023-05-24 17：04：32",
					text: "美加优选新品持续上线中",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281039002.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281039001.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038592.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038593.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038592.jpg",
					],
				},
				box2: {
					h: "溶脂塑型",
					time: "2023-05-24 17：03：07",
					text: "打造少女线  打造轮廓线 ",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281039001.jpg",
					]
				},
				box3: {
					h: "乐美加五大帮扶天团",
					time: "2023-05-24 17：01：55",
					text: "融招天团：专攻招商会议招商   股东招募   预售策划   开业策划店销天团：专攻门店门店拓客  业绩爆破  活动策划   产品供应直播天团：专攻线上社群运营    线上裂变    新品秒杀  持续复购技术天团：专供技术人才复制   新品考核   技术培训   技术帮扶动力天团：专攻内训修自己    修团队   修目标   修结果为品牌方运营保驾护航！",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_20231028103859.jpg",
					]
				},
				box4: {
					h: "乐美加亿计划股东密训",
					time: "2023-05-23 20：09：08",
					text: "愿景突围 目标突围 行动突围 结果突围",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038582.jpg",
					]
				},
				box5: {
					h: "全品械二类医用产品",
					time: "2023-05-23 16：09：22",
					text: "浅导美学激活",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038581.jpg",
					]
				},
				box6: {
					h: "乐美加优选正式上线",
					time: "2023-05-23 15：53：18",
					text: "为消费者甄选最优产品为品牌一站式输出平台",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_20231028103858.jpg",
					]
				},
				box7: {
					h: "品牌孵化杭州站圆满结束",
					time: "2023-05-23 15：39：48",
					text: "杭州华颜国际会议招商陪跑",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/2.mp4",
					]
				},
				box8: {
					h: "乐美加1980新套餐正式上线",
					time: "2023-05-23 15：34：07",
					text: "1980面部任选1组产品",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038571.jpg",
					]
				},
				box9: {
					h: "乐美加品牌创始人会议",
					time: "2023-05-23 15：27：03",
					text: "乐美加集团品牌创人会议-深圳站圆满结束",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_20231028103750.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_20231028103856.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_20231028103857.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038561.jpg",
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/微信图片_202310281038562.jpg",
					]
				},
				box10: {
					h: "双美运营系统",
					time: "2023-05-23 15：20：52",
					text: "轻医美转型双美    医美运营双美美容院升级双美    加盟双美连锁",
					image: [
						"https://edu-010327.oss-cn-beijing.aliyuncs.com/demo/23dbfa0d9f1c7a5d97117a6296cee71.jpg",

					]
				},
			}
		},
		onLoad() {

		},
		methods: {
			previewImage(index) {
				const urls = this.imageUrls;
				uni.previewImage({
					urls,
					current: urls[index]
				});
			},
			copyText(boxId) {
				console.log(boxId);
				let textToCopy = "";
				if (boxId === 1) {
					textToCopy = this.box1.text;

				} else if (boxId === 2) {
					textToCopy = this.box2.text;
				} else if (boxId === 3) {
					textToCopy = this.box3.text
				} else if (boxId === 4) {
					textToCopy = this.box4.text
				} else if (boxId === 5) {
					textToCopy = this.box5.text
				} else if (boxId === 6) {
					textToCopy = this.box6.text
				} else if (boxId === 7) {
					textToCopy = this.box7.text
				} else if (boxId === 8) {
					textToCopy = this.box8.text
				} else if (boxId === 9) {
					textToCopy = this.box9.text
				} else if (boxId === 10) {
					textToCopy = this.box10.text
				}
				uni.setClipboardData({
					data: textToCopy,
					success() {
						uni.showToast({
							title: '复制成功',
							icon: 'none'
						});
					}
				});
			},
			downloadMedia(imageArray) {
				// 遍历图片数组，依次下载并保存到手机相册
				imageArray.forEach((image) => {
					uni.downloadFile({
						url: image,
						success: (res) => {
							if (res.statusCode === 200) {
								// 保存图片到手机相册
								uni.saveImageToPhotosAlbum({
									filePath: res.tempFilePath,
									success: () => {
										uni.showToast({
											title: '下载成功',
											icon: 'success'
										});
									},
									fail: (err) => {
										console.error(err)
										uni.showToast({
											title: '下载失败',
											icon: 'none'
										});
									}
								});
							} else {
								uni.showToast({
									title: '下载失败',
									icon: 'none'
								});
							}
						},
						fail: (err) => {
							console.error(err)
							uni.showToast({
								title: '下载失败',
								icon: 'none'
							});
						}
					});
				});
			}

		}
	}
</script>

<style>
	.content {
		background-color: #f5f5f5;
		padding: 10rpx;
	}

	.box {
		background-color: #fff;
		margin-bottom: 20rpx;
	}

	.box-t view:nth-child(1) {
		font-weight: bold;
		margin-bottom: 10rpx;
	}

	.box-t view:nth-child(2) {
		color: #b3b5bd;
		font-weight: 400;
		margin-bottom: 20rpx;
		font-size: 30rpx
	}

	.box-t view:nth-child(3) {
		font-weight: normal;
		font-size: 32rpx;
		margin-bottom: 20rpx;

	}

	.box-c {
		width: 100%;
	}

	image {
		width: 233rpx;
		height: 233rpx;
		margin-right: 10rpx;
		margin-bottom: 10rpx;
	}

	.box-b {
		width: 100%;
		height: 100rpx;
		display: flex;
		border-top: 1px solid #ccc;
		justify-content: space-around;
		line-height: 100rpx;
	}

	.maxPhoto {
	    width: 100%;
	    height: 100%;
	    position: fixed;
	    background-color: black;
	    top: 0;
	    left: 0;
	    display: flex; /* 使用Flex布局 */
	    align-items: center; /* 垂直居中 */
	    justify-content: center; /* 水平居中 */
	    z-index: 999; /* 使其位于整个页面的上层，可以根据需要调整z-index的值 */
	}
	
	.maxPhoto image {
	    max-width: 100%;
	    max-height: 100%;
	}
	
	/* 其他样式保持不变 */

	
	video{
		
	}
	
</style>
