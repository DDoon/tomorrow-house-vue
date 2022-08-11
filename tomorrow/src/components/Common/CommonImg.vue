<template>
	<picture>
		<source />
		<img :src="imgSrc" :alt="imgAlt" />
	</picture>
</template>

<script>
export default {
	name: 'CommonImg',
	props: {
		imgSrc: {
			type: String,
			required: true,
		},
		imgAlt: {
			type: String,
			required: true,
		},
	},
};
</script>
