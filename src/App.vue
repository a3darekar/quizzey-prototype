<template>
	<div id="app">
		<Nav :nav_link.sync="active_nav_link" @changeNavLink="active_nav_link = $event"/>
		<div id="data">
			<div v-if="active_nav_link == 1">
				<Quiz />
			</div>
			<div v-else-if="active_nav_link == 2">
				## About
			</div>
			<div v-else-if="active_nav_link == 3">
				Contact
			</div>
		</div>
	</div>
</template>

<script>
import Quiz from './components/Quiz.vue'
import Nav from './components/Nav.vue'

export default {
	name: 'App',
	components: {
		Quiz,
		Nav
	},
	data() {
		return {
			active_nav_link : 1
		};
	},
};
</script>

<style>
body {
	background: #fd746c;
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
}
</style>
