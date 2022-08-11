<template>
	<div id="app">
		<TheHeader />
		<ProductDetailReviewList />
		<product-detail-page />
		<TheFooter />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TheFooter from '@/components/Layouts/TheFooter.vue';
import TheHeader from '@/components/Layouts/TheHeader.vue';
import ProductDetailReviewList from '@/components/ProductDetail/ProductDetailReviewList.vue';
import ProductDetailPage from './view/ProductDetailPage.vue';

@Component({
	components: {
		TheHeader,
		TheFooter,
		ProductDetailReviewList,
		ProductDetailPage,
	},
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '~@/assets/scss/common.scss';
</style>
