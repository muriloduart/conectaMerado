<!-- Mobile projects view -->
<template>
	<section>
		<div class="row">
			<ProjectCard :img="product_one" :txt="text_one" />
			<ProjectCard :txt="text_two" />
		</div>
		<div class="row"></div>
	</section>
</template>

<script>
import ProjectCard from '../ProjectCard.vue';
import mobDesign01 from '../../../assets/Padrinho.jpg';

export default {
	name: 'MobTab',
	data() {
		return {
			product_one: `<img src=${mobDesign01} alt="Mobile design" style="border-radius: 2.5rem; width: 100%; max-width: 100%;"/>`,
			text_two:
				'O Programa de Padrinhos é uma iniciativa emocionante e gratificante no Mercado Social. Ao premiar os padrinhos com selos de contribuidor e fornecer um incentivo fiscal ao maior contribuidor, buscamos promover e recompensar a cultura de compartilhamento e colaboração. Junte-se a nós, torne-se um padrinho e faça parte de uma comunidade que valoriza a generosidade, a sustentabilidade e o reconhecimento dos contribuidores. Sua participação fará a diferença!',
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
