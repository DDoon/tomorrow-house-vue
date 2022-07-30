<template>
	<aside class="sidebar sm-only">
		<header class="sidebar-header">
			<h1 class="logo">
				<a href="/">
					<img src="@/assets/images/logo.svg" alt="내일의 집" />
				</a>
			</h1>

			<!-- NOTE: 로그인을 한 경우  -->
			<div class="sidebar-user">
				<a href="/">
					<div class="avatar-24">
						<img src="@/assets/images/img-user-01.jpg" alt="사달라 아저씨" />
					</div>
					<strong class="username">사달라</strong>
				</a>
			</div>

			<!-- NOTE: 로그인을 하지 않은 경우  -->
			<!-- <div class="sidebar-auth">
          <a class="btn-outlined btn-40" href="/">로그인</a>
          <a class="btn-primary btn-40" href="/">회원가입</a>
        </div> -->
		</header>

		<nav class="sidebar-nav">
			<h2 class="visually-hidden">메뉴</h2>

			<div class="drawer-menu is-community">
				<button class="drawer-menu-button" type="button">
					<i class="ic-community" aria-hidden></i>
					커뮤니티
					<i class="ic-chevron" aria-hidden></i>
				</button>

				<div class="drawer-menu-content">
					<ul class="drawer-menu-list">
						<li
							v-for="item in sidebarItems"
							:key="item.id"
							class="drawer-menu-item"
						>
							<a :to="item.link">{{ item.title }}</a>
						</li>
					</ul>
				</div>
			</div>

			<div class="drawer-menu is-store is-active is-open">
				<button class="drawer-menu-button" type="button">
					<i class="ic-store" aria-hidden></i>
					스토어
					<i class="ic-chevron" aria-hidden></i>
				</button>

				<div class="drawer-menu-content">
					<ul class="drawer-menu-list">
						<li
							v-for="item in drawerItems"
							:key="item.id"
							class="drawer-menu-item"
						>
							<a href="/">스토어</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">카테고리</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">신혼가구</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">베스트</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">오늘의딜</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">연휴특가</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">월동준비</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">리퍼마켓</a>
						</li>
						<li class="drawer-menu-item is-active">
							<a href="/">
								기획전
								<i class="ic-new" lang="en" aria-label="New"></i>
							</a>
						</li>
					</ul>
				</div>
			</div>

			<div class="drawer-menu is-expert">
				<button class="drawer-menu-button" type="button">
					<i class="ic-expert" aria-hidden></i>
					인테리어시공
					<i class="ic-chevron" aria-hidden></i>
				</button>

				<div class="drawer-menu-content">
					<ul class="drawer-menu-list">
						<li class="drawer-menu-item">
							<a href="/">시공홈</a>
						</li>
						<li class="drawer-menu-item">
							<a href="/">시공스토어</a>
						</li>
					</ul>
				</div>
			</div>

			<!-- NOTE: 로그인을 한 경우  -->
			<div class="sidebar-user-menu">
				<ul class="user-menu-list">
					<li class="user-menu-item">
						<a href="/">마이페이지</a>
					</li>
					<li class="user-menu-item">
						<a href="/">나의 쇼핑</a>
					</li>
					<li class="user-menu-item">
						<a href="/">스크랩북</a>
					</li>
					<li class="user-menu-item">
						<a href="/">알림</a>
					</li>
					<li class="user-menu-item">
						<a href="/">이벤트</a>
					</li>
				</ul>
			</div>
		</nav>
	</aside>
</template>

<script>
export default {
	name: 'TheSidebar',
	props: {
		isActive: {
			type: Boolean,
			require: true,
		},
	},
	data() {
		return {
			sidebarItems: [
				{
					id: 1,
					link: '/main',
					title: '홈',
				},
				{
					id: 2,
					link: '/main',
					title: '사진',
				},
				{
					id: 3,
					link: '/main',
					title: '집들이',
				},
				{
					id: 4,
					link: '/main',
					title: '노하우',
				},
				{
					id: 5,
					link: '/main',
					title: '전문가집들이',
				},
				{
					id: 6,
					link: '/main',
					title: '셀프가이드',
				},
				{
					id: 7,
					link: '/main',
					title: '질문과답변',
				},
				{
					id: 8,
					link: '/main',
					title: '이벤트',
				},
			],
		};
	},
};
</script>
