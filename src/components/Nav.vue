<template>
	<div id="nav">
		<nav>
			<ul>
				<li data-dedata="0px" :class="{ active : nav_link == 1 }" @click="activate_link(1)">Quiz</li>
				<li data-dedata="160px" :class="{ active : nav_link == 2 }" @click="activate_link(2)">About</li>
				<li data-dedata="320px" :class="{ active : nav_link == 3 }" @click="activate_link(3)">Contact</li>
			</ul>
		</nav>
	</div>
</template>

<script>

export default {
	name: 'Nav',
	props: ['nav_link'],
	methods: {
		activate_link:function(el) {
			this.nav_link = el;
			this.$emit('changeNavLink', this.nav_link);
		}
	}
};
</script>

<style>
#nav {
	position: relative;
	margin: 50px auto;
	padding-bottom: 40px;
	width: 720px;
}

ul {
	border: 1px solid #fff;
	position: absolute;
	width: 100%;
	padding: 0;
	z-index: 100;
}

li:hover {
	background: rgba(255,255,255,.1);
}

.active {
	color: #fd746c;
	background: #fff;
}

nav ul li {
	display: inline-block;
	list-style: none;
	width: 243px;
	text-align: center;
	font-family: Helvetica, sans-serif;
	border: 1px dashed rgba(255,255,255, 0);
	padding: 10px 0 10px 0;
	color: #fff;
	margin: -1px -5px -1px -1px;
	cursor: pointer;
	transition: all .2s;
}
</style>
