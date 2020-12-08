<template>
	<nav class="nav">
		<ul class="nav__links">
			<li class="nav__link">
				<NuxtLink to="/">Home</NuxtLink>
			</li>
			<li class="nav__link">
				<NuxtLink to="/coming-soon">About</NuxtLink>
			</li>
			<li class="nav__link">
				<NuxtLink to="/coming-soon">Blog</NuxtLink>
			</li>
		</ul>
	</nav>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_utils.scss';

.nav {
	&__link {
		display: inline-block;
		vertical-align: middle;
		margin-right: $defVal * 2;
		font-size: 18px;

		opacity: 0.6;

		&:hover,
		&:focus,
		&--active {
			opacity: 1;
		}
	}
}
</style>
