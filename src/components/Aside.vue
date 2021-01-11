<template>
	<aside class="aside" ref="aside">
		<div class="aside__logo"></div>
		<nav class="aside__nav">
			<router-link to="/">
				<div class="aside__icon">
					<svg class="aside__icon-svg" fill="#000000" xmlns="http://www.w3.org/2000/svg"  viewBox="0 0 26 26" width="26px" height="26px">
						<path d="M 20 2.03125 C 19.449219 2.03125 19 2.480469 19 3.03125 L 19 7.8125 L 13.71875 2.53125 C 13.328125 2.140625 12.671875 2.140625 12.28125 2.53125 L 0.5625 14.28125 C 0.171875 14.671875 0.171875 15.296875 0.5625 15.6875 C 0.953125 16.078125 1.578125 16.078125 1.96875 15.6875 L 13 4.65625 L 24.0625 15.71875 C 24.257813 15.914063 24.523438 16.03125 24.78125 16.03125 C 25.039063 16.03125 25.273438 15.914063 25.46875 15.71875 C 25.859375 15.328125 25.859375 14.703125 25.46875 14.3125 L 22 10.84375 L 22 3.03125 C 22 2.480469 21.550781 2.03125 21 2.03125 Z M 13 6.5 L 2 17.5 L 2 23 C 2 24.65625 3.34375 26 5 26 L 21 26 C 22.65625 26 24 24.65625 24 23 L 24 17.5 Z M 11 16 L 15 16 C 15.550781 16 16 16.449219 16 17 L 16 23 C 16 23.550781 15.550781 24 15 24 L 11 24 C 10.449219 24 10 23.550781 10 23 L 10 17 C 10 16.449219 10.449219 16 11 16 Z"/>
					</svg>
				</div>
				<!-- <div>Главная</div> -->
				<!-- Главная -->
			</router-link>
			<router-link to="/about">
				<div class="aside__icon">
					<svg class="aside__icon-svg" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 415.744 415.744" style="enable-background:new 0 0 415.744 415.744;" xml:space="preserve">
						<path d="M207.872,0c-53.76,0-97.28,43.52-97.28,97.28s43.52,97.28,97.28,97.28s97.28-43.52,97.28-97.28S261.632,0,207.872,0z"/>
						<path d="M245.76,205.824h-75.776c-76.288,0-138.24,61.952-138.24,138.24v56.32c0,8.704,6.656,15.36,15.36,15.36H368.64c8.704,0,15.36-6.656,15.36-15.36v-56.32C384,267.776,322.048,205.824,245.76,205.824z"/>
					</svg>
				</div>
				
				<!-- Обо мне -->
			</router-link>
			<router-link to="/portfolio">
				<div class="aside__icon">
					<svg class="aside__icon-svg" id="bold" enable-background="new 0 0 24 24" height="512" viewBox="0 0 24 24" width="512" xmlns="http://www.w3.org/2000/svg">
						<path d="m15 6.5c-.552 0-1-.448-1-1v-1.5h-4v1.5c0 .552-.448 1-1 1s-1-.448-1-1v-1.5c0-1.103.897-2 2-2h4c1.103 0 2 .897 2 2v1.5c0 .552-.448 1-1 1z"/>
						<path d="m12.71 15.38c-.18.07-.44.12-.71.12s-.53-.05-.77-.14l-11.23-3.74v7.63c0 1.52 1.23 2.75 2.75 2.75h18.5c1.52 0 2.75-1.23 2.75-2.75v-7.63z"/>
						<path d="m24 7.75v2.29l-11.76 3.92c-.08.03-.16.04-.24.04s-.16-.01-.24-.04l-11.76-3.92v-2.29c0-1.52 1.23-2.75 2.75-2.75h18.5c1.52 0 2.75 1.23 2.75 2.75z"/>
					</svg>
				</div>
				
				<!-- Портфолио -->
			</router-link>
			<router-link to="/contacts">
				<div class="aside__icon">
					<svg class="aside__icon-svg" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 513.64 513.64" style="enable-background:new 0 0 513.64 513.64;" xml:space="preserve">
						<path d="M499.66,376.96l-71.68-71.68c-25.6-25.6-69.12-15.359-79.36,17.92c-7.68,23.041-33.28,35.841-56.32,30.72c-51.2-12.8-120.32-79.36-133.12-133.12c-7.68-23.041,7.68-48.641,30.72-56.32c33.28-10.24,43.52-53.76,17.92-79.36l-71.68-71.68c-20.48-17.92-51.2-17.92-69.12,0l-48.64,48.64c-48.64,51.2,5.12,186.88,125.44,307.2c120.32,120.32,256,176.641,307.2,125.44l48.64-48.64C517.581,425.6,517.581,394.88,499.66,376.96z"/>
					</svg>
				</div>
			
				<!-- Контакты -->
			</router-link>
		</nav>
		<div>
			<div class="aside__settings"></div>
			<div class="aside__icon  aside__icon--arrow" @click="switchAside">
				<svg class="aside__icon-svg" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px" viewBox="0 0 512 512" style="enable-background:new 0 0 512 512;" xml:space="preserve">
					<path d="M506.134,241.843c-0.006-0.006-0.011-0.013-0.018-0.019l-104.504-104c-7.829-7.791-20.492-7.762-28.285,0.068c-7.792,7.829-7.762,20.492,0.067,28.284L443.558,236H20c-11.046,0-20,8.954-20,20c0,11.046,8.954,20,20,20h423.557l-70.162,69.824c-7.829,7.792-7.859,20.455-0.067,28.284c7.793,7.831,20.457,7.858,28.285,0.068l104.504-104c0.006-0.006,0.011-0.013,0.018-0.019C513.968,262.339,513.943,249.635,506.134,241.843z"/>
				</svg>
			</div>
		</div>
	</aside>
</template>

<script>
export default {
	name: 'Aside',
	data() {
		return {
			showAside: false,
		}
	},
	methods: {
		switchAside: function() {
			this.showAside = !this.showAside;
			const app = document.querySelector('#app');

      if (this.showAside) {
				this.$refs.aside.classList.add('aside--show');
				app.style.gridTemplateColumns = '10em auto';
      } else {
				this.$refs.aside.classList.remove('aside--show');
				app.style.gridTemplateColumns = '3em auto';
			}
		}
	}
}
</script>

<style lang="scss">
	.aside {
		display: flex;
		flex-direction: column;
		justify-content: space-between;

		height: 100vh;

		background-color: var(--main-bg);
		border-right: 1px solid var(--main-color);

		&__nav {
			display: flex;
			flex-direction: column;
			
			& a {
				// position: relative;

				// width: 2em;
				// height: 2em;
				// padding: .5em;

				outline: none;
				transition: .15s;
			}
		}

		&__icon {
			position: relative;

			width: 2em;
			height: 2em;
			padding: 0.5em;

			cursor: pointer;
			transition: 0.15s;

			&:hover {
				transform: scale(1.2)
			}

			&--arrow {
				width: 100%;
				padding: 0.5em 0;

				transition: .3s;

				.aside--show & {
					transform: scaleX(-1);
				}

				&:hover {
					transform: translateX(7%);

					.aside--show & {
						transform: translateX(-7%) scaleX(-1);;
					}
				}
			}
		}

		&__icon-svg {
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);

			width: calc(100% - 1.5em);
			height: calc(100% - 1.5em);
		}
	}
</style>