<template>
	<header>
		<app-nav />
	</header>
	<main>
		<HeroContent />

		<AsideLists />

		<article-lists />
	</main>
	<footer>
		<TheAttribution />
	</footer>
</template>

<script setup>
import AppNav from "@/components/AppNav.vue";
import HeroContent from "@/components/HeroContent.vue";
import AsideLists from "./components/AsideLists.vue";
import ArticleLists from "./components/ArticleLists.vue";
import TheAttribution from "./components/TheAttribution.vue";
import { gsap } from 'gsap';
import { onMounted } from "vue";

const tl = gsap.timeline({
	ease: 'power4.out',
	onComplete: () => {
		gsap.from(["header", ".nav", ".hero", "aside", ".article__card", "attribution"], {
			clearProps: true
		})
	}
});

onMounted(() => {
	tl
		.from("header", {
			autoAlpha: 0.01,
		})
		.from(".nav", {
			autoAlpha: 0.01,
			y: -20,
		})
		.from(".hero", {
			autoAlpha: 0.01,
			x: -50,
			ease: "back.out",
			duration: 1.2,
		})
		.from("aside", {
			autoAlpha: 0.01,
			x: 20,
		})
		.from(".article__card", {
			autoAlpha: 0.01,
			y: 20,
			stagger: 0.2
		})
		.from(".attribution", {
			autoAlpha: 0.01,
			y: 20,
		})
})

</script>

<style scoped></style>
