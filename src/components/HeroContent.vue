<template>
	<section class="hero">
    <section class="hero__img">
      <picture>
        <source srcset="@/assets/images/image-web-3-desktop.jpg" media="(min-width: 800px)">
        <img src="@/assets/images/image-web-3-mobile.jpg" alt="web 3 banner">
      </picture>
    </section>
		<div class="content">
			<h1 class="title">The Bright Future of Web 3.0?</h1>
			<div class="description">
				<p class="text">
					We dive into the next evolution of the web that claims to put the
					power of the platforms back into the hands of the people. But is it
					really fulfilling its promise?
				</p>
				<!-- i didn't use routerlink here because this project is just a landing page without routiing capabilities -->
				<a href="#" class="cta">Read more</a>
			</div>
		</div>
	</section>
</template>

<script setup></script>

<style scoped>
.hero__img img {
  height: 280px;
  width: 100%;
  object-fit: cover;
  object-position: top;
}
</style>
