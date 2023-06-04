<!-- Web projects view -->
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
import minify from '../../../assets/mercado.webp';
import ant from '../../../assets/mercado.webp';
import lumy from '../../../assets/Padrinho.jpg';
import keeper from '../../../assets/Padrinho.jpg';

export default {
	name: 'WebTab',
	data() {
		return {
			product_one: `<img src=${minify} alt="Texto" style="border-radius: 2.5rem; max-width: 100%; width:100%;" />`,
			product_two: `<img src=${ant} alt="Personal portofolio" style="border-radius: 2.5rem; max-width: 100%; width: 100%;"/>`,
			text_two:
				'O Mercado Social é um projeto revolucionário que combina compras colaborativas, sustentabilidade e um sistema de pontuação inovador baseado na disponibilidade de produtos. Ao incentivar a colaboração, equilibrar a oferta e demanda e estimular a economia local, o sistema de pontuação do Mercado Social promove uma experiência de compras única e benéfica para todos os usuários. Junte-se a nós nessa jornada e faça parte de uma comunidade que valoriza a sustentabilidade e o compartilhamento de recursos.',
			product_three: `<img src=${lumy} alt="Dashboard UI Kit" style="border-radius: 2.5rem; max-width: 100%; width: 100%;"/>`,
			text_three: 'Lumy - Dashboard UI Kit',
			product_four: `<img src=${keeper} alt="Soccer Site" style="border-radius: 2.5rem; max-width: 100%; width: 100%;"/>`,
			text_four: 'Keeper - Soccer Site',
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
