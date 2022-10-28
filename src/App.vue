<template>
	<app-nav />
	<main>
		<section class="hero">
			<div class="hero__img"></div>
			<div class="content">
				<h1 class="title">The Bright Future of Web 3.0?</h1>
				<div class="description">
					<p class="text">
						We dive into the next evolution of the web that claims to put the
						power of the platforms back into the hands of the people. But is it
						really fulfilling its promise?
					</p>
					<a href="#" class="cta">Read more</a>
				</div>
			</div>
		</section>
		<aside>
			<h2 class="heading">New</h2>
			<div class="card">
				<h3 class="card__heading">Hydrogen VS Electric Cars</h3>
				<p>Will hydrogen-fueled cars ever catch up to EVs?</p>
			</div>
			<div class="card">
				<h3 class="card__heading">The Downsides of AI Artistry</h3>
				<p>
					What are the possible adverse effects of on-demand AI image
					generation?
				</p>
			</div>
			<div class="card">
				<h3 class="card__heading">Is VC Funding Drying Up?</h3>
				<p>
					Private funding by VC firms is down 50% YOY. We take a look at what
					that means.
				</p>
			</div>
		</aside>
		<section class="articles">
			<article class="article__card">
				<img src="@/assets/images/image-retro-pcs.jpg" alt="" />
				<div class="article__content">
					<h2 class="article__heading-number">01</h2>
					<h3 class="article__heading-title">Reviving Retro PCs</h3>
					<p>What happens when old PCs are given modern upgrades?</p>
				</div>
			</article>
			<article class="article__card">
				<img src="@/assets/images/image-top-laptops.jpg" alt="" />
				<div class="article__content">
					<h2 class="article__heading-number">02</h2>
					<h3 class="article__heading-title">Top 10 Laptops of 2022</h3>
					<p>Our best picks for various needs and budgets.</p>
				</div>
			</article>
			<article class="article__card">
				<img src="@/assets/images/image-gaming-growth.jpg" alt="" />
				<div class="article__content">
					<h2 class="article__heading-number">03</h2>
					<h3 class="article__heading-title">The Growth of Gaming</h3>
					<p>How the pandemic has sparked fresh opportunities.</p>
				</div>
			</article>
		</section>
	</main>
	<div>
		<div class="attribution">
			Challenge by
			<a href="https://www.frontendmentor.io?ref=challenge" target="_blank"
				>Frontend Mentor</a
			>. Coded by <a href="#">Your Name Here</a>.
		</div>
	</div>
</template>

<script>
import AppNav from "@/components/AppNav.vue";
export default {
	name: "App",
	components: {
		AppNav,
	},
};
</script>

<style scoped></style>
