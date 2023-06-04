<!-- Freebies projects view -->
<template>
	<section>
		<div class="row">
			<ProjectCard :img="product_one" :txt="text_one" />
			<ProjectCard :txt="text_two" />
		</div>
		<div class="row">
			<ProjectCard :img="product_three" :txt="text_three" />
			<ProjectCard :txt="text_four" />
		</div>
	</section>
</template>

<script>
import ProjectCard from '../ProjectCard.vue';
import freebies01 from '../../../assets/medalhas-de-fita-em-fundo-branco-prata-dourada-e-bronze_613284-652.avif';

export default {
	name: 'FreebiesTab',
	data() {
		return {
			product_one: `<img src=${freebies01} alt="Freebies" style="border-radius: 2.5rem; width: 100%; max-width: 100%;"/>`,
			text_two:
				'O Programa de Reconhecimento Empresarial do Mercado Social oferece uma oportunidade única para as empresas se destacarem como apoiadoras ativas da causa social. Ao receber selos de reconhecimento, além de visibilidade como forma de divulgação da empresa no eventos socias nos quais a prefeitura promover e incentivos fiscais adicionais, as empresas são reconhecidas por seu engajamento, impacto positivo e compromisso com a sustentabilidade. Junte-se a nós, torne-se uma empresa apoiadora e faça parte de uma comunidade que valoriza o envolvimento empresarial em prol de uma sociedade mais justa e colaborativa. Sua participação será fundamental para impulsionar mudanças positivas e promover um impacto',
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
