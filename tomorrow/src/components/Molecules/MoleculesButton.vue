<template>
	<AtomsButton :btnClass="btnClass" :btnWidth="btnWidth" :btnText="btnText">
		<AtomsIcon :iconClass="iconClass"></AtomsIcon>
		<i class="ic-chevron"></i>
	</AtomsButton>
</template>

<script>
import AtomsButton from '../Atoms/AtomsButton.vue';
import AtomsIcon from '../Atoms/AtomsIcon.vue';
export default {
	components: { AtomsButton, AtomsIcon },
	name: 'MoleculesButton',
	data() {
		return {
			btnClass: 'btn-primary btn-40',
			btnText: '글쓰기',
			iconClass: 'ic-chevron',
		};
	},
};
</script>
