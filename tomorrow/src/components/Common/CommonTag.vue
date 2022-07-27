<template>
	<strong :class="tagClass">{{ tagText }}</strong>
</template>

<script>
export default {
	name: 'CommonTag',
	props: {
		tagClass: {
			type: String,
			required: true,
		},
		tagText: {
			type: String,
			required: true,
		},
	},
};
</script>
