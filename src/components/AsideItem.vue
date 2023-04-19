<template>
	<section class="card">
		<h1 class="card__heading">{{ aside.title }}</h1>
		<p>{{ aside.content }}</p>
	</section>
</template>

<script setup>
defineProps({
  aside: {
    type: Object,
    required: true
  }
})
</script>