<template>
	<div class="layout">
		<site-header />
		<Nuxt class="layout__main" />
	</div>
</template>

<style lang="scss" scoped>
.layout {
	height: 100vh;

	display: flex;
	flex-direction: column;

	&__main {
		flex-grow: 1;
	}
}
</style>
