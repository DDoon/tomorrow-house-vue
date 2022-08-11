<template>
	<div class="container">
		<div class="row">
			<div class="col-sm-4">
				<AtomsButton
					:btnClass="primary.btnPrimary"
					:btnWidth="primary.btnWidth"
					:btnText="primary.btnText"
					:type="primary.btnType"
					disabled
				/>
				<AtomsButton
					:btnClass="outlined.btnOutlined"
					:btnWidth="outlined.btnWidth"
					:btnText="outlined.btnText"
					:type="outlined.btnType"
					disabled
				/>
				<molecules-button />
			</div>
		</div>
	</div>
</template>

<script>
import AtomsButton from '@/components/Atoms/AtomsButton.vue';
import MoleculesButton from '@/components/Molecules/MoleculesButton.vue';
export default {
	components: { AtomsButton, MoleculesButton },
	name: 'ProductDetailPage',
	data() {
		return {
			primary: {
				btnPrimary: 'btn-primary btn-56',
				btnWidth: {
					width: '200px',
				},
				btnText: 'Primary',
				btnType: 'button',
			},
			outlined: {
				btnOutlined: 'btn-outlined btn-56',
				btnWidth: {
					width: '200px',
				},
				btnText: 'Outlined',
				btnType: 'button',
			},
		};
	},
};
</script>
