<template>
	<div id="app">
		<TheHeader />
		<CommonTag :tagClass="tagRed" :tagText="tagPrice" />
		<CommonTag :tagClass="tagGray" :tagText="tagDelivery" />
		<CommonTag :tagClass="tagGreen" :tagText="tagReview" />
		<TheFooter />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TheFooter from './components/Layouts/TheFooter.vue';
import TheHeader from './components/Layouts/TheHeader.vue';
import CommonTag from './components/Common/CommonTag.vue';

@Component({
	components: { TheHeader, TheFooter, CommonTag },
	data() {
		return {
			tagRed: 'tag-red',
			tagGreen: 'tag-green',
			tagGray: 'tag-gray',
			tagPrice: '특가',
			tagDelivery: '무료배송',
			tagReview: '첫 리뷰 두 배 적립',
		};
	},
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '~@/assets/scss/common.scss';
</style>
