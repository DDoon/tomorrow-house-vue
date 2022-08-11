<template>
	<ol class="review-list">
		<li v-for="(item, idx) in reviewList" :key="idx" class="review-item">
			<article class="review-card">
				<header class="review-card-header">
					<h3 class="visually-hidden">{{ item.userName }}님이 좋아합니다</h3>

					<a class="avatar-24" href="/">
						<CommonImg :imgsrc="imgSrc" :alt="imgAlt" />
					</a>
					<div class="info">
						<a class="username" href="/">
							<strong>{{ item.userName }}</strong></a
						>
						<div class="detail">
							<CommonStarRating
								:starRatingClass="starRatingClass"
								:starRatingAria="starRatingAria"
							/>

							<div class="misc">
								<time>2021.01.01 </time>
								<span> 오늘의 집 구매</span>
							</div>
						</div>
					</div>
				</header>

				<div class="review-card-body">
					<p>
						집 전체를 데운다기보다는 틀어놓고 앞에 앉아있으면 따땃해지는
						정도예요. 불 꺼놓고 난로 켜고 담요 덮은 채로 커피 마시면 아주
						좋아요. 고양이도 좋아해요
					</p>
				</div>
				<footer class="review-card-footer">
					<CommonButton
						:btnClass="btnClass"
						:btnWidth="btnWidth"
						:btnText="btnText"
						type="button"
					/>

					<p>
						<strong><span>3</span>명</strong>에게 도움이 되었습니다.
					</p>
				</footer>
			</article>
		</li>
	</ol>
</template>

<script>
import CommonImg from '../Common/CommonImg.vue';
import CommonStarRating from '../Common/CommonStarRating.vue';
import CommonButton from '../Common/CommonButton.vue';
export default {
	name: 'ProductDetailReviewList',
	components: { CommonImg, CommonStarRating, CommonButton },

	data() {
		return {
			starRatingCalss: 'star-rating-13',
			starRatingAria: '5.0/5.0',
			imgSrc: '@/assets/images/img-user-02.jpg',
			imgAlt: '유저 이미지',
			btnClass: 'btn-outlined btn-32',
			btnText: '도움이 돼요',
			reviewList: [
				{
					userName: '김버그',
				},
			],
		};
	},
};
</script>
