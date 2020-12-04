<template>
	<div class="contact">
		<section>
			<h1 class="name">Developed by Amey Darekar</h1>
		</section>
		<section>
			<h3>
				<span class="roles">
					<i> Freelance Software Engineer</i>
				</span>
				<span class="location"> based in <i>Pune, India</i></span>
			</h3>
		</section>

		<section class="spotlight inset">
			<a href="http://github.com/a3darekar/" target="_blank" rel="nofollow noopener noreferrer" class="button xlarge dark primary glyph-code" style="background-color:#fff; color:#fd746c; border-color:#fff; padding: 10px 30px; border-radius: 15px;">
				<b>Visit me on GitHub</b>
			</a>
		</section>
		<section>
			<div style="padding: 20px 160px;">
				<p>I am a student and software engineer currently living in Pune, India. My interests range from reading to video games. I am also interested in food and movies.</p>
				<p>You can click the button above to view my repo. If you’d like to get in touch, feel free to say hello through any of the social links below.</p>
				<ul>
					<li>
						<a href="mailto:darekar.amey@gmail.com">
							<i class="fa fa-2x fa-envelope" aria-hidden="true"></i>
						</a>&nbsp;&nbsp;&nbsp;
					</li>
					<li>
						<a href="https://www.linkedin.com/in/a3darekar/">
							<i class="fa fa-2x fa-linkedin-square"></i>
						</a>&nbsp;&nbsp;&nbsp;
					</li>
					<li>
						<a href="twitter.com/a3darekar">
							<i class="fa fa-2x fa-twitter"></i>
						</a>
					</li>
				</ul>
			</div>
		</section>
	</div>
</template>

<script>
export default {

	name: 'Quiz',

	data () {
		return {

		}
	}
};
</script>

<style lang="css" scoped>
.contact {
	text-align: center;
	border: 1px solid #fff;
	align-content: center;
	margin: 80px 160px;
}

a {
	margin: 10px 0; 
	color: #fff;
	text-decoration: underline;

}

ul {
	border: none;
	position: relative;
}

ul li {
	display: inline; 
	list-style: none;
	padding: 20px;
}

.inset {
	padding: 20px;
}
</style>