<template>
	<div class="quiz">
		<div v-for="(component, index) in steps" :key="component">
			<div v-if="currentStep == index">
				<component :is="component" :currentStep.sync="currentStep" @updateCurrentStep="updateCurrentStep"/>
			</div>
		</div>
	</div>
</template>

<script>
import Intro from './Intro.vue'
import Details from './Details.vue'
import Section1 from './Section1.vue'
import Section2 from './Section2.vue'
import Section3 from './Section3.vue'
import Results from './Results.vue'

export default {

	name: 'Quiz',
	components: {
		Intro, Details, Section1, Section2, Section3, Results
	},
	data () {
		return {
			steps: ['Intro', 'Details', 'Section1', 'Section2', 'Section3', 'Results'],
			currentStep: 0,
			Responses: null,
			questions: null
		}
	},
	methods: {
		updateCurrentStep(val) {
			this.currentStep = val
		}
	}
};
</script>

<style lang="css" scoped>
.quiz {
	text-align: center;
	vertical-align: middle;
	margin: 80px 160px;
	padding: 20px;
	border: 1px solid #fff;
}

.button {
	background-color:#fff;
	color:#fd746c;
	border-color:#fff;
	border-radius: 15px;
	padding: 10px 30px;
	margin: 60px;
	cursor: pointer;
}
</style>