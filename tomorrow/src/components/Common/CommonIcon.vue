<template>
	<button :class="iconClass" :aria-label="iconAria">
		<i :class="iconShapeLeft" aria-hidden="true"></i>
		{{ btnText }}
		<i :class="iconShapeRight" aria-hidden="true"></i>
	</button>
</template>

<script>
export default {
	name: 'CommonIcon',
	props: {
		iconClass: {
			type: String,
			required: true,
		},
		iconShapeLeft: {
			type: String,
		},
		iconShapeRight: {
			type: String,
		},
		iconAria: {
			type: String,
			required: true,
		},
		btnText: {
			type: String,
		},
	},
};
</script>
