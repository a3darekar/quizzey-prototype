<template>
	<content>
		<h3>
			Well Done!
		</h3>
		You did better than 70% other participants... I think.
		In the real application, you will get evaluation or some insight on your performance of the quiz here. Since I am not collecting any responses its hard for me to evaluate.
		<br>
		<br>Sorry for your troubles. Here's a compilation video of cute kittens.
		<br>
		<br>
		<iframe width="560" height="315" src="https://www.youtube.com/embed/WBnqQaUCM1M" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe> 
		<br>
		<br>
		<a class="button" @click="terminate"><b>Retake the Quiz</b></a>
	</content>
</template>

<script>
export default {

	name: 'Intro',
	props: ['currentStep'],
	data () {
		return {
			step: this.currentStep,
		}
	},

	methods: {
		terminate() {
			this.step = 0;
			this.$emit('updateCurrentStep', this.step);
		}
	}

};
</script>

<style lang="css" scoped>

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