<!-- Freebies projects view -->
<template>
	<section>
		<div class="row">
			<ProjectCard :img="product_one" />
			<ProjectCard :txt="text_two" />
		</div>
		<div class="row"></div>
	</section>
</template>

<script>
import ProjectCard from '../ProjectCard.vue';
import freebies01 from '../../../assets/estoque.png';

export default {
	name: 'FreebiesTab',
	data() {
		return {
			product_one: `<img src=${freebies01} alt="Freebies" style="border-radius: 2.5rem; width: 100%; max-width: 100%;"/>`,
			text_two:
				'O Sistema de Pontuação de Estoque do Mercado Social é uma abordagem inovadora que valoriza a necessidade dos produtos no mercado. Ao atribuir pontuações com base na demanda e disponibilidade, o sistema promove uma distribuição mais equitativa e sustentável. Junte-se a nós nessa jornada e faça parte de uma comunidade que valoriza a colaboração, a circulação de produtos e o aproveitamento consciente dos recursos. Sua participação será fundamental para criar um mercado mais justo, eficiente e colaborativo.',

			text_three: 'Pontuação de acordo com a necessidade do Estoque',
			text_four: 'Keeper - Freebies',
		};
	},
	components: {
		ProjectCard,
	},
};
</script>

<style scoped>
.row {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
@media (max-width: 767px) {
	.row {
		flex-direction: column;
	}
}
</style>
