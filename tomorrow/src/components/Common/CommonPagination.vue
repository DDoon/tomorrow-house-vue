<template>
	<div class="pagination">
		<button
			class="page-control page-prev"
			type="button"
			aria-label="이전페이지로 이동"
		>
			<i class="ic-chevron" aria-hidden="true"></i>
		</button>
		<ol class="page-list">
			<li class="page-item">
				<a href="/">1</a>
			</li>
			<li class="page-item is-active">
				<a href="/">2</a>
			</li>
			<li class="page-item">
				<a href="/">3</a>
			</li>
			<li class="page-item">
				<a href="/">4</a>
			</li>
			<li class="page-item">
				<a href="/">5</a>
			</li>
		</ol>
		<button
			class="page-control page-next"
			type="button"
			aria-label="다음페이지로 이동"
		>
			<i class="ic-chevron" aria-hidden="true"></i>
		</button>
	</div>
</template>

<script>
export default {
	name: 'CommonPagination',
};
</script>
