<template>
	<div id="app">
		<TheHeader />

		<TheFooter />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TheFooter from '@/components/Layouts/TheFooter.vue';
import TheHeader from '@/components/Layouts/TheHeader.vue';
import CommonAnchorIcon from '@/components/Common/CommonAnchorIcon.vue';

@Component({
	components: { TheHeader, TheFooter, CommonAnchorIcon },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '~@/assets/scss/common.scss';
</style>
