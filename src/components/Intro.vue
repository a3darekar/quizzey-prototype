<template>
	<content>
		<h2>
			Quiz
		</h2>
		Feel free to explore this example site and try out the quiz for the prototype by clicking the button below.
		<br>
		<br>
		<br>

		<a class="button" @click="proceed"><b>Lets get started</b></a>
		<br>
		<br>
		<br>
		(Since it doesn't have any backend support, I wont get any responses you provide here, and this example is only to represent the intended working of the prototype. Please do share your feedback through e-mail or any social media channels 😅)
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
</style>