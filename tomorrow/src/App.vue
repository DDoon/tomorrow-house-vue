<template>
	<div id="app">
		<TheHeader />
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

<style></style>
