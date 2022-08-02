<template>
	<div
		@click.self="offSidebar"
		class="overlay sm-only"
		aria-hidden="true"
	></div>
</template>

<script>
export default {
	name: 'TheOverlay',

	methods: {
		offSidebar() {
			this.$emit('offSidebar', { isActive: this.isActive });
		},
	},
};
</script>
