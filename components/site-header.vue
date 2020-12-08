<template>
	<header class="header pad--x-4 pad--y-3">
		<div class="header__wrapper max-width--1120">
			<Logo class="header__logo" />
			<site-nav />
		</div>
	</header>
</template>

<script>
import siteNav from './site-nav.vue'
export default {
	components: { siteNav },
}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_utils.scss';

.header {
	width: 100%;
	position: fixed;
	// box-shadow: $bRadius $defVal $defVal * 5
	// 	transparentize($color: $secondary, $amount: 0.8);

	&__wrapper {
		// padding: $defVal * 2 $defVal;

		> * {
			display: inline-block;
			vertical-align: middle;
		}
	}

	&__logo {
		padding-right: $defVal * 2;
	}
}
</style>
