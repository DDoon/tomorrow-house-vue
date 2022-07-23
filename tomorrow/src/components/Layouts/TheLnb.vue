<template>
	<nav class="lnb">
		<div class="container">
			<div class="row">
				<div class="col-sm-12">
					<h1 class="visually-hidden">스토어 메뉴</h1>
					<ul class="lnb-list">
						<!-- 커뮤니티 일시 -->
						<!--	<template>
							<li
								v-for="(lnb, index) in lnbCommunity"
								:key="index"
								class="lnb-item"
							>
								<a :to="lnb.link"
									>{{ lnb.title }}
									<i :class="lnb.icon" lang="en" aria-label="New"></i>
								</a>
							</li>
						</template> -->

						<!-- 스토어 일시 -->
						<template>
							<li
								v-for="(lnb, index) in lnbStore"
								:key="index"
								class="lnb-item"
							>
								<a :to="lnb.link"
									>{{ lnb.title }}
									<i :class="lnb.icon" lang="en" aria-label="New"></i>
								</a>
							</li>
						</template>

						<!-- 맞춤업체찾기 일시 -->
						<!-- <template>
							<li v-for="(lnb, index) in lnbFindCompany" :key="index" class="lnb-item">
								<a :to="lnb.link"
									>{{ lnb.title }}
									<i :class="lnb.icon" lang="en" aria-label="New"></i>
								</a>
							</li>
						</template> -->
					</ul>
				</div>
			</div>
		</div>
	</nav>
</template>

<script>
export default {
	name: 'TheLnb',
	data() {
		return {
			lnbCommunity: [
				{
					title: '홈',
					link: '/main',
				},
				{
					title: '팔로잉',
					link: '/main',
				},
				{
					title: '사진',
					link: '/main',
				},
				{
					title: '집들이',
					link: '/main',
				},
				{
					title: '노하우',
					link: '/main',
				},
				{
					title: '전문가집들이',
					link: '/main',
				},
				{
					title: '셀프가이드',
					link: '/main',
				},
				{
					title: '질문과답변',
					link: '/main',
				},
				{
					title: '3D인테리어',
					link: '/main',
				},
				{
					title: '이벤트',
					link: '/main',
				},
			],
			lnbStore: [
				{
					title: '스토어',
					link: '/main',
				},
				{
					title: '카테고리',
					link: '/main',
				},
				{
					title: '오늘의딜',
					link: '/main',
				},
				{
					title: '7월주방세일',
					link: '/main',
					icon: 'ic-new',
				},
				{
					title: '주말반짝특가',
					link: '/main',
					icon: 'ic-new',
				},
				{
					title: '오!굿즈',
					link: '/main',
					icon: 'ic-new',
				},
				{
					title: '빠른배송',
					link: '/main',
				},
				{
					title: '프리미엄',
					link: '/main',
					icon: 'ic-new',
				},
				{
					title: '기획전',
					link: '/main',
				},
			],
			lnbFindCompany: [
				{
					title: '홈',
					link: '/main',
				},
				{
					title: '인테리어시공',
					link: '/main',
				},
				{
					title: '이사',
					link: '/main',
				},
				{
					title: '설치수리',
					link: '/main',
				},
				{
					title: '우리동네아파트',
					link: '/main',
				},
			],
		};
	},
};
</script>
