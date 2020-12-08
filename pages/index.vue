<template>
	<main class="main">
		<section class="section bday__section pad--x-4">
			<div class="section__wrapper bday__wrapper max-width--1120">
				<header class="section__header bday__header">
					<p class="section__txt bday__txt">You deserve a</p>
					<!-- prettier-ignore -->
					<h1 class="section__caption bday__caption">Happy Birthday! ✨</h1>
				</header>
				<div class="bday-media__cont">
					<div class="bday-media__obj bday-media__love-1 img-cont">
						<img src="/img/love-face.png" alt="" />
					</div>
					<div class="bday-media__obj bday-media__baloons img-cont">
						<img src="/img/baloons.png" alt="" />
					</div>
				</div>
			</div>
		</section>
	</main>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
@import '~/assets/scss/_utils.scss';

.bday {
	&__section {
		height: 100%;
	}

	&__wrapper {
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	&__caption {
		font-size: 72px;
		color: var(--secondary);

		@supports (font-size: clamp(48px, 5vw, 80px)) {
			font-size: clamp(48px, 5vw, 80px);
		}
	}

	&__txt {
		font-size: 22px;
	}
}

.bday-media {
	&__cont {
		position: absolute;
		width: 100%;
		height: 100%;
		pointer-events: none;
		overflow: hidden;
	}

	&__obj {
		position: absolute;
		max-width: 200px;
		max-height: 200px;
		pointer-events: all;
		animation: float 3s ease-in 0.012s infinite alternate-reverse;

		@for $var from 0 through 5 {
			&:nth-of-type(#{$var}) {
				animation-duration: $var + s;
			}
		}
	}

	&__baloons {
		bottom: -$defVal * 2;
		left: -$defVal;
	}

	&__love {
		&-1 {
			top: -$defVal * 2;
			right: -$defVal;
			max-width: 160px;
		}
	}
	@media screen and (min-width: 500px) {
		&__baloons {
			max-width: 400px;
			max-height: 400px;
		}
	}

	@keyframes float {
		from {
			transform: translateY(0);
		}
		to {
			transform: translateY(#{$defVal + 5px});
		}
	}
}
</style>
