<template>
	<button :style="btnWidth">{{ btnText }}</button>
</template>
<script>
export default {
	name: 'CommonButton',
	props: {
		btnWidth: {
			width: null,
			required: true,
		},
		btnText: {
			type: String,
		},
	},
};
</script>
