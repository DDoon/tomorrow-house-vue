<template>
	<button :class="btnClass" :style="btnWidth">{{ btnText }}</button>
</template>
<script>
export default {
	name: 'CommonButton',
	props: {
		btnClass: {
			width: null,
		},
		btnWidth: {
			width: null,
		},
		btnText: {
			type: String,
		},
	},
};
</script>
