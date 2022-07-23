<template>
	<div id="app">
		<TheHeader />
		<router-view></router-view>
	</div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import TheHeader from './components/Layouts/TheHeader.vue';

@Component({
	components: { TheHeader },
})
export default class App extends Vue {}
</script>

<style lang="scss">
@import '~@/assets/scss/common';
</style>
