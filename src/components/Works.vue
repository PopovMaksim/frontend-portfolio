<template>
	<section class="works  container">
		<div class="works__header" :class="{works__header_notitle: !sub}">
			<h2 class="subtitle" v-if="sub">Портфолио</h2>
			<div class="works__icons">
				<div
					class="works__icon"
					:class="{ works__icon_active: viewMode === 'works__container--tile' }"
					v-on:click="viewMode = 'works__container--tile' "
				>
					<svg class="works__icon-svg" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
						viewBox="0 0 30 30" style="enable-background:new 0 0 30 30;" xml:space="preserve">
						<path class="st0" d="M13,14H1c-0.6,0-1-0.4-1-1V1c0-0.6,0.4-1,1-1h12c0.6,0,1,0.4,1,1v12C14,13.6,13.6,14,13,14z"/>
						<path class="st0" d="M17,14h12c0.6,0,1-0.4,1-1V1c0-0.6-0.4-1-1-1H17c-0.6,0-1,0.4-1,1v12C16,13.6,16.4,14,17,14z"/>
						<path class="st0" d="M17,16h12c0.6,0,1,0.4,1,1v12c0,0.6-0.4,1-1,1H17c-0.6,0-1-0.4-1-1V17C16,16.4,16.4,16,17,16z"/>
						<path class="st0" d="M13,16H1c-0.6,0-1,0.4-1,1v12c0,0.6,0.4,1,1,1h12c0.6,0,1-0.4,1-1V17C14,16.4,13.6,16,13,16z"/>
					</svg>
				</div>
				<div
					class="works__icon"
					:class="{ works__icon_active: viewMode === 'works__container--list' }"
					v-on:click="viewMode = 'works__container--list' "
				>
					<svg class="works__icon-svg" version="1.1" id="Слой_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
							viewBox="0 0 30 30" style="enable-background:new 0 0 30 30;" xml:space="preserve">
						<path class="st0" d="M11,8h18c0.6,0,1-0.4,1-1V1c0-0.6-0.4-1-1-1H11c-0.6,0-1,0.4-1,1v6C10,7.6,10.4,8,11,8z"/>
						<path class="st0" d="M11,30h18c0.6,0,1-0.4,1-1v-6c0-0.6-0.4-1-1-1H11c-0.6,0-1,0.4-1,1v6C10,29.6,10.4,30,11,30z"/>
						<path class="st0" d="M11,19h18c0.6,0,1-0.4,1-1v-6c0-0.6-0.4-1-1-1H11c-0.6,0-1,0.4-1,1v6C10,18.6,10.4,19,11,19z"/>
						<path class="st0" d="M7,8H1C0.4,8,0,7.6,0,7V1c0-0.6,0.4-1,1-1h6c0.6,0,1,0.4,1,1v6C8,7.6,7.6,8,7,8z"/>
						<path class="st0" d="M7,19H1c-0.6,0-1-0.4-1-1v-6c0-0.6,0.4-1,1-1h6c0.6,0,1,0.4,1,1v6C8,18.6,7.6,19,7,19z"/>
						<path class="st0" d="M7,30H1c-0.6,0-1-0.4-1-1v-6c0-0.6,0.4-1,1-1h6c0.6,0,1,0.4,1,1v6C8,29.6,7.6,30,7,30z"/>
					</svg>
				</div>
			</div>
			
		</div>
		<div class="works__container" v-bind:class="viewMode">
			<div class="works__item" v-for="item of items" v-bind:key="item.id">
				<div class="works__image">
					<!-- <img alt="" class="works__image-img" > -->
					<picture>
						<source :srcset="item.imageWebp" type="image/webp">
						<img class="works__image-img" :src="item.image" :alt="item.title">
					</picture>
				</div>
				<div class="works__info">
					<div class="works__item-main">
						<h4 class="works__item-title">{{ item.title }}</h4>
						<p class="works__text">{{ item.content }}</p>
					</div>
					<div class="works__item-footer">
						<div class="works__btns">
							<a :href="item.links.preview" class="works__btn" target="_blank">Просмотр</a>
							<a
								v-if="item.links.git"
								:href="item.links.git"
								class="works__btn"
								target="_blank"
							>GitHub</a>
						</div>
						<div class="works__technology-stack">
							<div class="works__technology-stack-item" v-for="tec of item.technologyStack" :key="tec.id">{{ tec }}</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</section>
</template>
<script>

	export default {
		name: 'Works',
		props: {
			sub: Boolean,
		},
		data() {
			return {
				viewMode: 'works__container--tile',
				items: [
					{
						title: 'Портфолио',
						content: 'Проект на Vue CLI',
						image: require('@/assets/works/portfolio.jpg'),
						imageWebp: require('@/assets/works/portfolio.webp'),
						links: {
							preview: 'https://popovmaksim.github.io',
							git: 'https://github.com/PopovMaksim/frontend-portfolio', 
						},
						technologyStack: [
							'Vue',
							'Vue Router'
						],
					},
					{
						title: 'Кейс Клиника 2.0',
						content: 'Адаптивная и кроссбраузерная верстка кейса, анимирование всех элементов, реализация слайдера через API "Swiper"',
						image: require('@/assets/works/medicinskij.jpg'),
						imageWebp: require('@/assets/works/medicinskij.webp'),
						links: {
							preview: 'https://vladit.ru/portfolio/kejs-medicinskij/',
						},
						technologyStack: [
							'HTML',
							'CSS',
							'JavaScript',
						],
					},
					{
						title: 'Кейс умного дома',
						content: 'Адаптивная и кроссбраузерная верстка кейса, анимирование всех элементов, реализация слайдера через API "Swiper"',
						image: require('@/assets/works/smart-house.jpg'),
						imageWebp: require('@/assets/works/smart-house.webp'),
						links: {
							preview: 'https://vladit.ru/portfolio/kejs-smart-house/',
						},
						technologyStack: [
							'HTML',
							'CSS',
							'JavaScript',
						],
					},
					{
						title: 'Кейс ипотечной платформы',
						content: 'Адаптивная и кроссбраузерная верстка кейса, анимирование всех элементов, реализация слайдера через API "Swiper"',
						image: require('@/assets/works/ipoteka-global.jpg'),
						imageWebp: require('@/assets/works/ipoteka-global.webp'),
						links: {
							preview: 'https://vladit.ru/portfolio/kejs-ipoteka-global/',
						},
						technologyStack: [
							'HTML',
							'CSS',
							'JavaScript',
						],
					},
					{
						title: 'Кейс "Мустанг"',
						content: 'Адаптивная и кроссбраузерная верстка кейса, анимирование всех элементов, реализация слайдера через API "Swiper"',
						image: require('@/assets/works/mustang.jpg'),
						imageWebp: require('@/assets/works/mustang.webp'),
						links: {
							preview: 'https://vladit.ru/portfolio/kejs-mustang/',
						},
						technologyStack: [
							'HTML',
							'CSS',
							'JavaScript',
						],
					},
					{
						title: 'Bicycle',
						content: 'Кроссбраузерная адаптивная верстка главной страницы с помощью Grid Layout',
						image: require('@/assets/works/bicycle.jpg'),
						imageWebp: require('@/assets/works/bicycle.webp'),
						links: {
							preview: 'https://popovmaksim.github.io/Bicycle',
							git: 'https://github.com/PopovMaksim/bicycle', 
						},
						technologyStack: [
							'HTML',
							'CSS',
							'JavaScript',
						],
					},
					{
						title: 'Minima',
						content: 'Верстка макета с помощью flexbox',
						image: require('@/assets/works/minima.jpg'),
						imageWebp: require('@/assets/works/minima.webp'),
						links: {
							preview: 'https://popovmaksim.github.io/Minima',
							git: 'https://github.com/PopovMaksim/Minima', 
						},
						technologyStack: [
							'HTML',
							'CSS',
							'jQuery',
						],
					},
					{
						title: 'Adele',
						content: 'Верстка макета с помощью Grid Layout, слайдер выполнен на чистом css',
						image: require('@/assets/works/adele.jpg'),
						imageWebp: require('@/assets/works/adele.webp'),
						links: {
							preview: 'https://popovmaksim.github.io/Adele',
							git: 'https://github.com/PopovMaksim/Adele', 
						},
						technologyStack: [
							'HTML',
							'CSS',
						],
					},
					{
						title: 'LeRestaurante',
						content: 'Верстка макета с помощью flexbox',
						image: require('@/assets/works/restaurante.jpg'),
						imageWebp: require('@/assets/works/restaurante.webp'),
						links: {
							preview: 'https://popovmaksim.github.io/LeRestaurant/',
							git: 'https://github.com/PopovMaksim/LeRestaurant', 
						},
						technologyStack: [
							'Pug',
							'SASS',
							'JavaScript',
							'Gulp',
						],
					},
				],
			}
		},
		methods: {
			//
		}
	}
</script>
<style lang="scss">
	.works {
		&__header {
			display: flex;
			justify-content: space-between;
			align-items: center;

			&_notitle {
				justify-content: flex-end;

				padding: 0 0 2em;
			}
		}

		&__icons {
			display: flex;
			align-items: center;
		}

		&__icon {
			position: relative;

			width: 1.5em;
			height: 1.5em;
			padding: 0.5em;

			cursor: pointer;
		}

		&__icon-svg {
			position: absolute;
			top: 0.5em;
			left: 0.5em;

			width: calc(100% - 1em);
		}

		&__container {
			display: flex;
			justify-content: space-between;
			flex-wrap: wrap;
		}

		&__item {
			position: relative;

			overflow: hidden;

			border-radius: 5px;
			box-shadow: 0 0 10px var(--main-color);

			transition: .5s;

			.works__container--tile & {

				@media (max-width: 750px) {
					width: 100%;
					margin-bottom: 4%;
				}				
				@media (min-width: 750px) and (max-width: 1000px) {
					width: 48.5%;
					margin-bottom: 3%;
				}				
				@media (min-width: 1000px) {
					width: 32%;
					margin-bottom: 2%;
				}
				
				&:hover {
					& .works__info {
						opacity: 1;
					}

					& .works__image::after {
						background-color: var(--main-bg);
						opacity: 0.9;
					}
				}
			}

			.works__container--list & {
				display: flex;

				width: 100%;
				margin-bottom: 4%;

				@media (max-width: 650px) {
					flex-direction: column;
				}
			}
		}

		&__image {
			position: relative;

			overflow: hidden;

			&::after {
				.works__container--tile & {
					content: "";
					position: absolute;
					top: 0;
					left: 0;
					z-index: 5;

					width: 100%;
					height: 100%;

					transition: .25s;
				}
			}

			.works__container--tile & {
				width: 100%;

				@media (max-width: 750px) {
					padding-top: 80%;
				}
				@media (min-width: 750px) {
					padding-top: 110%;
				}
			}

			.works__container--list & {

				@media (max-width: 650px) {
					width: 100%;
					padding-top: 68%;
				}
				@media (min-width: 650px) {
					width: 40%;

					&::after {
						content: "";
						position: absolute;
						top: 0;
						right: 0;

						border: 2em solid transparent;
						border-top: 20em solid var(--main-bg);
						border-right: 0 solid var(--main-bg);
					}
				}
				@media (min-width: 650px) and (max-width: 750px) {
					padding-top: 45%;
				}
				@media (min-width: 750px) and (max-width: 1000px) {
					padding-top: 35%;
				}
				@media (min-width: 1000px) {
					padding-top: 25%;
				}

				
			}
		}

		&__image-img {
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);

			width: 100%;

			transition: .5s;

			.works__item:hover & {
				transform: translate(-50%, -50%) scale(1.1);
			}
		}

		&__info {
			z-index: 15;

			display: flex;
			justify-content: space-between;
			flex-direction: column;

			margin: 1.5em 2em 1em;

			transition: .3s;

			@media (max-width: 750px) {
				margin: 1em 0.5em 0.5em;
			}

			.works__container--tile & {
				position: absolute;
				top: 0;
				left: 0;

				width: calc(100% - 4em);
				height: calc(100% - 2.5em);

				opacity: 0;
			}
		}

		&__item-title {
			margin: 0;
		}

		&__text {
			@media (max-width: 750px) {
				margin: 0.5em 0;
			}
		}

		&__btn {
			display: inline-block;

			padding: .25em .5em;

			color: var(--color-link);

			&:hover {
				text-decoration: underline;
			}
		}

		&__technology-stack-item {
			display: inline-block;
			
			margin: 0.25em;
			padding: .25em .5em;

			border-radius: 5px;
			box-shadow: 0 0 3px var(--main-color);

			font-size: 0.9rem;
		}
	}

	.st0 {
		fill:#B3B3B3;

		.works__icon_active & {
			fill: var(--main-color)
		}
	}
</style>