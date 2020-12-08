<template>
	<figure class="logo logo--m">
		<img class="logo__img" src="/icon.png" alt="" />
		<p class="logo__text logo__text-hide">Summer-blu</p>
	</figure>
</template>

<style lang="scss" scoped>
.logo {
	width: fit-content;
	display: inline-block;

	> * {
		display: inline-block;
		vertical-align: middle;
	}

	&:hover {
		.logo__text-hide {
			max-width: 199px;
		}
	}

	&--m {
		height: 38px;
	}

	&__img {
		height: 100%;
	}

	&__text {
		&-hide {
			max-width: 0px;
			overflow: hidden;
			white-space: nowrap;
		}
	}
}
</style>
