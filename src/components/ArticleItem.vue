<template>
	<article class="article__card">
		<img :src="`${getImageUrl(article.img)}`" :alt="article.alt" />
		<div class="article__content">
			<h2 class="article__heading--number">{{ article.titleNumber }}</h2>
			<h3 class="article__heading--title">{{ article.title }}</h3>
			<p>{{ article.content }}</p>
		</div>
	</article>
</template>

<script setup>
defineProps({
  article: {
    type: Object,
    required: true,
  }
})

function getImageUrl(name) {
  return new URL(`/src/assets/images/${name}`, import.meta.url).href
}
</script>

