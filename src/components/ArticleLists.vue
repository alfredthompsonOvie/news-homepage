<template>
  <section  class="articles">
    <ArticleItem v-for="article in articles" :key="article.title" :article="article"/>
  </section>
</template>

<script setup>
import ArticleItem from './ArticleItem.vue';
import { ref } from "vue";

const articles = ref([
	{
		img: 'image-retro-pcs.jpg',
    alt: "retro pcs",
		titleNumber: "01",
		title: 'Reviving Retro PCs',
		content: 'What happens when old PCs are given modern upgrades?'
	},
	{
		img: 'image-top-laptops.jpg',
    alt: "laptops",
		titleNumber: '02',
		title: 'Top 10 Laptops of 2022',
		content: 'Our best picks for various needs and budgets.'
	},
	{
		img: 'image-gaming-growth.jpg',
    alt: "gaming growth",
		titleNumber: '03',
		title: 'The Growth of Gaming',
		content: 'How the pandemic has sparked fresh opportunities.'
	},
])
</script>