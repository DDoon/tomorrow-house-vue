<template>
	<header class="global-header">
		<div class="gnb">
			<div class="container">
				<div class="row">
					<div class="col-sm-4">
						<i class="ic-chevron"></i>
						<i class="ic-close"></i>
						<div class="test">아아아아아아</div>
						<CommonButton
							:btnWidth="btnWidth"
							:btnText="btnText"
							class="btn-primary btn-40"
							type="button"
						/>
					</div>
				</div>
			</div>
		</div>
	</header>
</template>

<script>
import CommonButton from '../Common/CommonButton.vue';
export default {
	name: 'TheHeader',
	components: { CommonButton },
	data() {
		return {
			btnWidth: {
				width: '120px',
			},
			btnText: '테스트입니다',
		};
	},
};
</script>
