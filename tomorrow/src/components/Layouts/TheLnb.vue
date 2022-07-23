<template>
	<nav class="lnb">
		<div class="container">
			<div class="row">
				<div class="col-sm-12">
					<h1 class="visually-hidden">스토어 메뉴</h1>
					<ul class="lnb-list">
						<li v-for="(lnb, index) in lnbItem" :key="index" class="lnb-item">
							<a :to="lnb.link"
								>{{ lnb.title }}
								<i :class="lnb.icon" lang="en" aria-label="New"></i>
							</a>
						</li>
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
			lnbItem: [
				{
					title: '스토어',
					link: '/main',
				},
				{
					title: '카테고리',
					link: '/main',
				},
				{
					title: '신혼가구',
					link: '/main',
				},
				{
					title: '베스트',
					link: '/main',
				},
				{
					title: '오늘의딜',
					link: '/main',
				},
				{
					title: '연휴특가',
					link: '/main',
				},
				{
					title: '월동준비',
					link: '/main',
				},
				{
					title: '리퍼마켓',
					link: '/main',
					icon: 'ic-new',
				},
				{
					title: '기획전',
					link: '/main',
					icon: 'ic-new',
				},
			],
		};
	},
};
</script>
