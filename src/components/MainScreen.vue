<template>
	<section class="main-screen">
		<h1 class="main-screen__title">Front-end разработчик</h1>
	</section>
</template>

<script>
export default {
	name: 'MainScreen'
}
</script>

<style lang="scss">
	.main-screen {
		position: relative;

		display: flex;
		justify-content: center;
		align-items: center;

		width: 100%;
		height: 100vh;

		background: url("../assets/main-screen.svg") no-repeat center /cover;

		// &::after {
		// 	content: "";
		// 	position: absolute;
		// 	bottom: -7em;

		// 	width: 100%;
		// 	height: 7em;

		// 	background: linear-gradient(#3e4067, transparent);
		// }

		&__title {
			color: #3e4067;
			text-shadow: 0 0 15px #4e5077;

			font-family: 'Lobster';
			font-size: calc( 1rem + 5vw );
			font-weight: 900;
			text-align: center;
		}
	}
</style>