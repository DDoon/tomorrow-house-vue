<template>
	<button :class="iconClass" :aria-label="iconAria">
		{{ btnText }}
		<i :class="iconShape" aria-hidden="true"></i>
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
		iconShape: {
			type: String,
			required: true,
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
