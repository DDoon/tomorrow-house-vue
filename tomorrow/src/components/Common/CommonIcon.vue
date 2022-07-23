<template>
	<button :class="iconClass">
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
		},
		iconShape: {
			type: String,
			required: true,
		},
		btnText: {
			type: String,
		},
	},
};
</script>
