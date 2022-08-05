<template>
	<a href="/" :class="anchorClass" :aria-label="anchorAriaLabel">
		{{ anchorText }}
		<i :class="anchorIcon"></i>
	</a>
</template>

<script>
export default {
	name: 'CommonAnchorIcon',
	props: {
		anchorClass: {
			type: String,
		},
		anchorAriaLabel: {
			type: String,
		},
		anchorText: {
			type: String,
		},
		anchorIcon: {
			type: String,
		},
	},
};
</script>
