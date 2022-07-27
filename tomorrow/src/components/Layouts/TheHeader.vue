<template>
	<header class="global-header">
		<div class="gnb">
			<div class="container">
				<div class="row">
					<div class="col-sm-4">
						<div class="gnb-wrapper">
							<div class="gnb-left">
								<h1 class="logo">
									<a href="/">
										<img src="@/assets/images/logo.svg" alt="내일의 집" />
									</a>
								</h1>

								<nav class="gnb-nav sm-hidden">
									<h2 class="visually-hidden">메뉴</h2>
									<ul class="gnb-nav-list">
										<li class="gnb-nav-item"><a href="/">커뮤니티</a></li>
										<li class="gnb-nav-item is-active">
											<a href="/">스토어</a>
										</li>
										<li class="gnb-nav-item"><a href="/">맞춤업체찾기</a></li>
									</ul>
								</nav>

								<button
									class="gnb-icon-button is-menu sm-only"
									type="button"
									aria-label="메뉴 열기 버튼"
								>
									<i class="ic-menu"></i>
								</button>
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
												<li class="search-history-item">
													<button class="word-button" type="button">
														김버그
													</button>
													<button
														class="delete-button"
														type="button"
														aria-label="검색어 삭제"
													>
														<i class="ic-close"></i>
													</button>
												</li>
												<li class="search-history-item">
													<button class="word-button" type="button">
														버그
													</button>
													<button
														class="delete-button"
														type="button"
														aria-label="검색어 삭제"
													>
														<i class="ic-close"></i>
													</button>
												</li>
												<li class="search-history-item">
													<button class="word-button" type="button">
														튕김버그
													</button>
													<button
														class="delete-button"
														type="button"
														aria-label="검색어 삭제"
													>
														<i class="ic-close"></i>
													</button>
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

									<a
										class="gnb-icon-button sm-hidden"
										href="/"
										aria-label="스크랩북 페이지로 이동"
									>
										<i class="ic-bookmark"></i>
									</a>

									<a
										class="gnb-icon-button sm-hidden"
										href="/"
										aria-label="내 소식 페이지로 이동"
									>
										<i class="ic-bell"></i>
									</a>

									<a
										class="gnb-icon-button is-cart"
										href="/"
										aria-label="장바구니 페이지로 이동"
									>
										<i class="ic-cart"></i>
										<strong class="badge">5</strong>
									</a>

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
										</div>
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
									:iconClass="iconClass"
									:iconShape="iconChevron"
									:btnText="btnText"
									type="button"
								/>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<TheLnb />
	</header>
</template>

<script>
import CommonIcon from '@/components/Common/CommonIcon.vue';
import TheLnb from '@/components/Layouts/TheLnb.vue';
export default {
	components: { CommonIcon, TheLnb },
	name: 'TheHeader',
	data() {
		return {
			iconClass: 'btn-primary btn-40 sm-hidden',
			iconChevron: 'ic-chevron',
			btnText: '글쓰기',
		};
	},
};
</script>
