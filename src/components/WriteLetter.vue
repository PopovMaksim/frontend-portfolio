<template>
	<section class="letter  container">
		<h2 class="letter__title">Написать письмо</h2>
		<form class="letter__form" action="mailto:maksim-popov-1996@mail.ru" method="get" target="_blank">
			<input class="letter__input" type="text" name="subject" placeholder="Введите тему">
			<textarea class="letter__input  letter__input--body" name="body" rows="7" placeholder="Написать..."></textarea>
			<input class="letter__input  letter__input--submit" type="submit" value="Отправить">
		</form> 
	</section>
</template>

<script>

export default {
    name: 'WriteLetter'
    
}
</script>

<style lang="scss">
	.letter {

		&__title {
			margin: 0 0 0 3em;
			padding: 1em 0;

			font-family: 'Lobster';
			font-size: 2rem;
			font-weight: 700;
		}

		&__form	{
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			max-width: 500px;
			margin: 0 auto;

			font-size: 1.25rem;
		}

		&__input {
			box-sizing: border-box;
			width: 100%;
			padding: 0.75em 1em;
			margin: 2% 0;

			border: none;
			border-radius: 5px;
			box-shadow: 0 0 7px var(--main-color);
			background-color: var(--second-bg);
			outline: none;

			font-size: 1rem;

			&--body {
				resize: none;
			}

			&--submit {
				width: 14em;

				font-weight: 700;
				letter-spacing: 0.25em;
				text-transform: uppercase;

				cursor: pointer;
				transition: .1s;

				&:hover {
					background-color: var(--main-bg);
					box-shadow: 0 0 5px var(--main-color);
				}

				&:active {
					box-shadow: 0 0 3px var(--main-color);
				}
			}
		}
	}
</style>