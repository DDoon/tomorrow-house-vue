<template>
	<header class="global-header">
		<div class="gnb">
			<div class="container">
				<div class="row">
					<div class="col-sm-4">
						<div class="gnb-wrapper">
							<div class="gnb-left">
								<CommonLogo />

								<nav class="gnb-nav sm-hidden">
									<h2 class="visually-hidden">메뉴</h2>
									<ul class="gnb-nav-list">
										<li
											v-for="item in navList"
											:key="item.id"
											class="gnb-nav-item"
										>
											<a href="/">{{ item.text }}</a>
										</li>
									</ul>
								</nav>

								<CommonIcon
									@click.native="toggleSidebar"
									:iconClass="iconClass"
									:iconShapeLeft="iconMenu"
									:iconAria="iconAria"
									type="button"
								/>
							</div>

							<div class="gnb-right">
								<div class="gnb-search lg-only">
									<div class="input-group">
										<i class="ic-search" aria-hidden></i>
										<input
											class="form-input"
											type="text"
											placeholder="스토어 검색"
										/>
									</div>

									<section class="search-history">
										<header class="search-history-header">
											<h2 class="title">최근 검색어</h2>
											<button type="button">전체 삭제</button>
										</header>

										<div class="search-history-content">
											<ol class="search-history-list">
												<li
													v-for="item in searchList"
													:key="item.id"
													class="search-history-item"
												>
													<button class="word-button" type="button">
														{{ item.text }}
													</button>
													<CommonIcon
														:iconClass="item.btnClass"
														:iconAria="item.iconAria"
														:iconShapeLeft="item.iconClose"
														type="button"
													/>
												</li>
											</ol>
										</div>
									</section>
								</div>

								<!-- NOTE: 로그인을 한 경우  -->
								<div class="button-group">
									<button
										class="gnb-icon-button is-search lg-hidden"
										type="button"
										aria-label="검색창 열기 버튼"
									>
										<i class="ic-search"></i>
									</button>

									<CommonAnchorIcon
										v-for="item in anchorIconList"
										:key="item.id"
										:anchorClass="item.anchorClass"
										:anchorAriaLabel="item.anchorAriaLabel"
										:anchorIcon="item.anchorIcon"
									/>

									<div class="my-menu sm-hidden">
										<button
											class="my-menu-button"
											type="button"
											aria-label="마이메뉴 열기 버튼"
										>
											<!-- <img
												src="@/assets/images/img-user-01.jpg"
												alt="사달라 아저씨"
											/> -->
										</button>
										<!-- 
										<div class="my-menu-content">
											<ul class="my-menu-list">
												<li class="my-menu-item">
													<a href="/">마이페이지</a>
												</li>
												<li class="my-menu-item">
													<a href="/">나의 쇼핑</a>
												</li>
												<li class="my-menu-item">
													<a href="/">이벤트</a>
												</li>
												<li class="my-menu-item">
													<button type="button">로그아웃</button>
												</li>
											</ul>
										</div> -->
									</div>
								</div>

								<!-- NOTE: 로그인을 하지 않은 경우  -->
								<!-- <div class="button-group">
                    <button
                      class="gnb-icon-button is-search lg-hidden"
                      type="button"
                      aria-label="검색창 열기 버튼"
                    >
                      <i class="ic-search"></i>
                    </button>
                    <a
                      class="gnb-icon-button is-cart"
                      href="/"
                      aria-label="장바구니 페이지로 이동"
                    >
                      <i class="ic-cart"></i>
                    </a>

                    <div class="gnb-auth sm-hidden">
                      <a href="/">로그인</a>
                      <a href="/">회원가입</a>
                    </div>
                  </div> -->
								<CommonIcon
									:iconClass="btnClass"
									:btnText="btnText"
									:iconAria="btnAria"
									:iconShapeRight="icChevron"
								/>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<TheLnb />
		<div class="breadcrumb">
			<CommonAnchorIcon
				v-for="item in breadcrumbList"
				:key="item.id"
				:anchorAriaLabel="item.anchorAriaLabel"
				:anchorText="item.anchorText"
				:anchorIcon="item.anchorIcon"
			/>
		</div>
		<TheSidebar :class="isActiveSidebar" :isActive="isActive" />
		<TheOverlay :class="isActiveSidebar" @offSidebar="offSidebar" />
	</header>
</template>

<script>
import TheLnb from '@/components/Layouts/TheLnb.vue';
import TheSidebar from '@/components/Layouts/TheSidebar.vue';
import TheOverlay from '@/components/Layouts/TheOverlay.vue';
import CommonIcon from '@/components/Common/CommonIcon.vue';
import CommonLogo from '@/components/Common/CommonLogo.vue';
import CommonAnchorIcon from '@/components/Common/CommonAnchorIcon.vue';

export default {
	components: {
		TheLnb,
		TheSidebar,
		TheOverlay,
		CommonIcon,
		CommonLogo,
		CommonAnchorIcon,
	},
	name: 'TheHeader',
	data() {
		return {
			isActive: false,
			// CommoIcon
			iconClass: 'gnb-icon-button is-menu sm-only',
			iconMenu: 'ic-menu',
			iconAria: '메뉴 열기 버튼',
			title: '야야야야',
			btnClass: 'btn-primary btn-40 sm-hidden',
			btnText: '글쓰기',
			btnAria: '글쓰기 버튼',
			icChevron: 'ic-chevron',
			searchList: [
				{
					id: 1,
					btnClass: 'delete-button',
					iconAria: '검색어 삭제',
					iconClose: 'ic-close',
					text: '검색내용',
				},
			],
			navList: [
				{
					id: 1,
					text: '커뮤니티',
				},
				{
					id: 2,
					text: '스토어',
				},
				{
					id: 3,
					text: '맞춤업체찾기',
				},
			],
			anchorIconList: [
				{
					id: 1,
					anchorClass: 'gnb-icon-button sm-hidden',
					anchorAriaLabel: '스크랩북 페이지로 이동',
					anchorIcon: 'ic-bookmark',
				},
				{
					id: 2,
					anchorClass: 'gnb-icon-button sm-hidden',
					anchorAriaLabel: '내 소식 페이지로 이동',
					anchorIcon: 'ic-bell',
				},
				{
					id: 3,
					anchorClass: 'gnb-icon-button sm-hidden',
					anchorAriaLabel: '장바구니 페이지로 이동',
					anchorIcon: 'ic-cart',
				},
			],
			breadcrumbList: [
				{
					id: 1,
					anchorAriaLabel: '가전 페이지로 이동',
					anchorText: '가전',
					anchorIcon: 'ic-chevron',
				},
				{
					id: 2,
					anchorAriaLabel: '계절가전 페이지로 이동',
					anchorText: '계절가전',
					anchorIcon: 'ic-chevron',
				},
				{
					id: 3,
					anchorAriaLabel: '전기히터/온풍기 페이지로 이동',
					anchorText: '전기히터/온풍기',
					anchorIcon: 'ic-chevron',
				},
				{
					id: 4,
					anchorAriaLabel: '전기히터 페이지로 이동',
					anchorText: '전기히터',
					anchorIcon: 'ic-chevron',
				},
			],
		};
	},
	computed: {
		isActiveSidebar() {
			return this.isActive ? 'is-active' : false;
		},
	},
	methods: {
		toggleSidebar() {
			this.isActive = !this.isActive;
		},
		offSidebar() {
			this.isActive = false;
		},
	},
};
</script>
