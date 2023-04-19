<template>
	<aside>
		<h1 class="heading">New</h1>
    <AsideItem v-for="aside in asides" :key="aside.title" :aside="aside"/>
	</aside>
</template>

<script setup>
import { ref } from "vue";
import AsideItem from "./AsideItem.vue";

const asides = ref([
	{
		title: "Hydrogen VS Electric Cars",
		content: "Will hydrogen-fueled cars ever catch up to EVs?",
	},
	{
		title: "The Downsides of AI Artistry",
		content: "What are the possible adverse effects of on-demand AI image generation?",
	},
	{
		title: "Is VC Funding Drying Up?",
		content: "Private funding by VC firms is down 50% YOY. We take a look at what that means.",
	},
]);
</script>

<style lang="scss" scoped></style>
