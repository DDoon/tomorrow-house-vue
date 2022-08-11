<template>
	<i :class="iconClass"></i>
</template>

<script>
export default {
	name: 'AtomsIcon',
	props: {
		iconClass: {
			type: String,
			required: true,
		},
	},
};
</script>
