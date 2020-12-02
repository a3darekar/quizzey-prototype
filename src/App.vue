<template>
	<div id="app">
		<Nav :nav_link.sync="active_nav_link" @changeNavLink="active_nav_link = $event"/>
		<div id="data">
			<div v-if="active_nav_link == 1">
				<Quiz />
			</div>
			<div v-else-if="active_nav_link == 2">
				<div id="about">
					This site is created to serve as a prototype for a prospected project. This is developed by <a href="github.com/a3darekar">a3darekar</a>.
				</div>
			</div>
			<div v-else-if="active_nav_link == 3">
				<Contact />
			</div>
		</div>
	</div>
</template>

<script>
import Quiz from './components/Quiz.vue'
import Nav from './components/Nav.vue'
import Contact from './components/contact.vue'

export default {
	name: 'App',
	components: {
		Quiz,
		Contact,
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
	color: #fff;
}

a:link {
	color: #fff;
	text-decoration: underline;

}

#about {
	text-align: center;
	padding: 80px 40px;
	vertical-align: middle;
	margin: 80px 160px;
	border: 1px solid #fff;
}
</style>
