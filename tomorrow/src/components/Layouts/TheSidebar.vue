<template>
	<aside class="sidebar sm-only">
		<header class="sidebar-header">
			<CommonLogo />

			<!-- NOTE: 로그인을 한 경우  -->
			<!-- <div class="sidebar-user">
				<a href="/">
					<div class="avatar-24">
						<img src="@/assets/images/img-user-01.jpg" alt="사달라 아저씨" />
					</div>
					<strong class="username">사달라</strong>
				</a>
			</div> -->

			<!-- NOTE: 로그인을 하지 않은 경우  -->
			<div class="sidebar-auth">
				<a class="btn-outlined btn-40" href="/">로그인</a>
				<a class="btn-primary btn-40" href="/">회원가입</a>
			</div>
		</header>

		<nav class="sidebar-nav">
			<h2 class="visually-hidden">메뉴</h2>
			<div
				v-for="item in drawerItems"
				:key="item.id"
				:class="isActiveDrawer"
				class="drawer-menu is-community"
			>
				<CommonIcon
					@click="toggleDrawer"
					:iconClass="item.class"
					:iconAria="item.aria"
					:iconShapeLeft="item.iconLeft"
					:iconShapeRight="item.iconRight"
					:btnText="item.text"
					type="button"
				></CommonIcon>

				<div class="drawer-menu-content">
					<ul class="drawer-menu-list">
						<li
							v-for="drawer in item.drawerList"
							:key="drawer.id"
							:isActive2="isActive2"
							class="drawer-menu-item"
						>
							<a :to="drawer.link"
								>{{ drawer.title }}
								<i :class="drawer.icon" lang="en" aria-label="New"></i>
							</a>
						</li>
					</ul>
				</div>
			</div>

			<!-- NOTE: 로그인을 한 경우  -->
			<!-- <div class="sidebar-user-menu">
				<ul class="user-menu-list">
					<li
						v-for="item in drawerItemsMenu"
						:key="item.id"
						class="user-menu-item"
					>
						<a href="/"
							>{{ item.title }}
							<i :class="item.icon" lang="en" aria-label="New"></i>
						</a>
					</li>
				</ul>
			</div> -->
		</nav>
	</aside>
</template>

<script>
import CommonIcon from '@/components/Common/CommonIcon.vue';
import CommonLogo from '../Common/CommonLogo.vue';

export default {
	components: { CommonIcon, CommonLogo },
	name: 'TheSidebar',
	props: {
		isActive: {
			type: Boolean,
			require: true,
		},
	},
	data() {
		return {
			isActive2: false,

			drawerItems: [
				{
					id: 1,
					class: 'drawer-menu-button',
					aria: '메뉴열기',
					iconLeft: 'ic-store',
					iconRight: 'ic-chevron',
					text: '스토어',
					drawerList: [
						{
							id: 1,
							title: '카테고리',
							link: '/main',
						},
						{
							id: 2,
							title: '신혼가구',
							link: '/main',
						},
						{
							id: 3,
							title: '베스트',
							link: '/main',
						},
						{
							id: 4,
							title: '오늘의딜',
							link: '/main',
						},
						{
							id: 5,
							title: '연휴특가',
							link: '/main',
						},
						{
							id: 6,
							title: '월동준비',
							link: '/main',
						},
						{
							id: 7,
							title: '리퍼마켓',
							link: '/main',
						},
						{
							id: 8,
							title: '기획전',
							icon: 'ic-new',
							link: '/main',
						},
					],
				},
				{
					id: 2,
					class: 'drawer-menu-button',
					aria: '메뉴열기',
					iconLeft: 'ic-community',
					iconRight: 'ic-chevron',

					text: '커뮤니티',
					drawerList: [
						{
							id: 1,
							title: '카테고리',
						},
						{
							id: 2,
							title: '신혼가구',
						},
						{
							id: 3,
							title: '베스트',
						},
						{
							id: 4,
							title: '오늘의딜',
						},
						{
							id: 5,
							title: '연휴특가',
						},
						{
							id: 6,
							title: '월동준비',
						},
						{
							id: 7,
							title: '리퍼마켓',
						},
						{
							id: 8,
							title: '기획전',
							icon: 'ic-new',
						},
					],
				},
				{
					id: 3,
					class: 'drawer-menu-button',
					aria: '메뉴열기',
					iconLeft: 'ic-expert',
					iconRight: 'ic-chevron',
					text: '맞춤업체찾기',
					drawerList: [
						{
							id: 1,
							title: '카테고리',
						},
						{
							id: 2,
							title: '신혼가구',
						},
						{
							id: 3,
							title: '베스트',
						},
						{
							id: 4,
							title: '오늘의딜',
						},
						{
							id: 5,
							title: '연휴특가',
						},
						{
							id: 6,
							title: '월동준비',
						},
						{
							id: 7,
							title: '리퍼마켓',
						},
						{
							id: 8,
							title: '기획전',
							icon: 'ic-new',
						},
					],
				},
			],
		};
	},
	computed: {
		isActiveDrawer() {
			return this.isActive2 ? 'is-active is-open' : false;
		},
	},
	methods: {
		toggleDrawer() {
			this.isActive2 = !this.isActive2;
		},
	},
};
</script>
