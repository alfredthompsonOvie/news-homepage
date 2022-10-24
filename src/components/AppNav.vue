<template>
	<nav class="nav">
		<div class="brand">
			<img
				src="@/assets/images/logo.svg"
				alt="brand logo"
				class="brand__logo"
			/>
		</div>
		<div class="hamburger" v-if="isMobile" @click="toggleMobileNav">
			<img src="@/assets/images/icon-menu.svg" alt="menu icon" class="menu" />
		</div>
		<!-- mobile Nav -->
		<ul class="mobileNav" v-if="isMobile">
			<div class="close">
				<img
					src="@/assets/images/icon-menu-close.svg"
					alt="menu icon"
					class="menu"
				/>
			</div>

			<li>
				<a href="#">Home</a>
			</li>
			<li>
				<a href="#">New</a>
			</li>
			<li>
				<a href="#">Popular</a>
			</li>
			<li>
				<a href="#">Trending</a>
			</li>
			<li>
				<a href="#">Categories</a>
			</li>
		</ul>

		<!-- tablet/ desktop Nav -->
		<ul class="mainNav" v-if="!isMobile">
			<li>
				<a href="#">Home</a>
			</li>
			<li>
				<a href="#">New</a>
			</li>
			<li>
				<a href="#">Popular</a>
			</li>
			<li>
				<a href="#">Trending</a>
			</li>
			<li>
				<a href="#">Categories</a>
			</li>
		</ul>
	</nav>
</template>

<script>
export default {
	name: "AppNav",
	data() {
		return {
			isMobile: true,
			windowWidth: null,
		};
	},
	methods: {
		toggleMobileNav() {},
	},
};
</script>

<style scoped>
.nav {
	display: flex;
	justify-content: space-between;
	align-items: center;
}
.brand__logo {
	width: 3.5em;
}
.menu {
	/* width: 2.5em; */
	cursor: pointer;
}
.mobileNav {
	position: fixed;
	top: 0;
	bottom: 0;
	right: 0;
	width: 12em;
	background-color: #fff;
	padding: 2em;
  display: flex;
  flex-direction: column;
}
.close {
  margin-bottom: 5em;
  display: inline-block;
  margin-left: auto;
}
</style>
