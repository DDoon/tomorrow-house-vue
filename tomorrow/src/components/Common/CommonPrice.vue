<template>
	<div :class="priceClass">
		<strong class="amount">{{ item.amount }}</strong>
		<span class="currency">원</span>
	</div>
</template>

<script>
export default {
	name: 'CommonPrice',
	props: {
		priceClass: {
			type: String,
			required: true,
		},
	},
};
</script>
