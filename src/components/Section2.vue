<template>
	<content>
		<h3>Section #2</h3>
		<br>
		<br>
			Questions for section2
		<br>
		<br>
		<a class="button" @click="back"><b>Back</b></a>
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
</style>