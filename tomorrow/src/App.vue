<template>
	<div id="app">
		<TheHeader />
		<TheFooter />
		<TheSidebar />
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TheFooter from './components/Layouts/TheFooter.vue';
import TheHeader from './components/Layouts/TheHeader.vue';
import TheSidebar from './components/Layouts/TheSidebar.vue';

@Component({
	components: { TheHeader, TheFooter, TheSidebar },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '~@/assets/scss/common.scss';
</style>
