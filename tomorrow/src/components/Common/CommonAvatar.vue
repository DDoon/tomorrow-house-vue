<template>
	<div :class="avatarClass">
		<CommonImg />
	</div>
</template>

<script>
import CommonImg from './CommonImg.vue';
export default {
	name: 'CommonAvatar',
	components: { CommonImg },
	props: {
		avatarClass: {
			type: String,
			required: true,
		},
	},
};
</script>
