<template>
	<content>
		<h3>Please provide your details</h3>
		Details of the individuals taking the servey/quiz go here. Currently, the prototype does not persist any information. 
		<br>
		Enter any dummy information or leave the form blank. Click on Proceed button to go to first section.
		<br>
		<br>
		<label for="name">Enter your Name: </label>
		<input type="text" id="name">
		<br>
		<br>
		<label for="name">Enter your Email: </label>
		<input type="text" id="email">
		<br>
		<br>
		<a class="button" @click="back"><b>Go back to main site</b></a>
		<a class="button" @click="proceed"><b>Proceed</b></a>
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
		back() {
			this.step--;
			this.$emit('updateCurrentStep', this.step);
		},
		proceed() {
			this.step++;
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

label {
	padding-right: 10px;
}
</style>