<template>
	<section class="experience  container">
		<h2 class="subtitle">Опыт</h2>

		<div class="experience__category">
			<h3 class="experience__subtitle">Образование</h3>
			<div class="experience__item">
				<div class="experience__period">
					<div class="experience__date">2018</div>
					<div class="experience__qualification">Бакалавр</div>
				</div>
				<div class="experience__content">
					<h4 class="experience__name-organization">Ивановский государственный энергетический университет имени В. И. Ленина</h4>
					<h5 class="experience__info">Управление в технических системах</h5>
				</div>
			</div>
		</div>
		<div class="experience__category">
			<h3 class="experience__subtitle">Работа</h3>
			<div class="experience__item">
				<div class="experience__period">
					<span class="experience__date">2018</span>
					<span class="experience__date">-</span>
					<span class="experience__date">2020</span>
				</div>
				<div class="experience__content">
					<h4 class="experience__name-organization">МУ "Управление административными зданиями и транспортом"</h4>
					<h5 class="experience__position">Системный администратор</h5>
					<ul class="experience__info">
						<li>Техническое обслуживание ПК</li>
						<li>Администрирование локальных сетей</li>
						<li>Администрирование сервера (Windows Server 2012)</li>
						<li>Консультирование сотрудников по работе с компьютерной техникой</li>
						<li>Администрирование сайта на 1С-Битрикс</li>
						<li>Составление ТЗ на закупку нового оборудования</li>
					</ul>
				</div>
			</div>
			<div class="experience__item">
				<div class="experience__period">
					<div class="experience__date">2020</div>
					<div class="experience__date">-</div>
					<div class="experience__date  experience__date--small">наст.вр</div>
				</div>
				<div class="experience__content">
					<h4 class="experience__name-organization">Vlad IT</h4>
					<h5 class="experience__position">Front-end разработчик</h5>
					<ul class="experience__info">
						<li>Адаптивная и кроссбраузерная верстка</li>
						<li>Создание визуальных эффектов</li>
					</ul>
				</div>
			</div>
		</div>
	</section>
</template>

<script>
export default {
	name: 'Experience',
}
</script>

<style lang="scss">
	.experience {

		&__subtitle {
			margin: 1em 2em 2em;
		}

		&__item {
			display: flex;

			margin-bottom: 4%;
		}

		&__period {
			display: flex;
			flex-direction: column;
			align-items: center;

			margin-right: 5%;
		}

		&__date {
			font-size: 1.75rem;
			font-weight: 700;

			&--small {
				font-size: 1rem;
			}
		}

		&__qualification {
			font-size: 0.9rem;
			font-style: italic;
		}

		&__name-organization {
			margin: 0 0 0.5em;

			font-size: 1.1rem;
		}

		&__position {
			margin: 0;

			font-size: 1rem;
		}

		&__info {
			line-height: 1.3;
		}
	}

</style>