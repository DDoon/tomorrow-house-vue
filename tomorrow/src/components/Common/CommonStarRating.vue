<template>
	<div :class="starRatingClass" :aria-label="starRatingAria">
		<i class="ic-star"></i>
		<i class="ic-star"></i>
		<i class="ic-star"></i>
		<i class="ic-star"></i>
		<i class="ic-star"></i>
	</div>
</template>

<script>
export default {
	name: 'CommonStarRating',
	props: {
		starRatingClass: {
			type: String,
			required: true,
		},
		starRatingAria: {
			type: String,
			required: true,
		},
	},
};
</script>
