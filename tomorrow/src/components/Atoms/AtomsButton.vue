<template>
	<button :class="btnClass" :style="btnWidth">
		{{ btnText }}
	</button>
</template>

<script>
export default {
	name: 'AtomsButton',
	props: {
		btnClass: {
			type: String,
		},
		btnWidth: {
			type: String,
			width: null,
		},
		btnText: {
			type: String,
		},
	},
};
</script>
