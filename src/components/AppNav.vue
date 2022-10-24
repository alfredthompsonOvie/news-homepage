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
		<ul class="mobileNav" v-show="mobileNav" @click="toggleMobileNav">
			<div class="close">
				<img
					src="@/assets/images/icon-menu-close.svg"
					alt="menu icon"
					class="menu"
				/>
			</div>

			<li>
				<a href="#" class="nav__link">Home</a>
			</li>
			<li>
				<a href="#" class="nav__link">New</a>
			</li>
			<li>
				<a href="#" class="nav__link">Popular</a>
			</li>
			<li>
				<a href="#" class="nav__link">Trending</a>
			</li>
			<li>
				<a href="#" class="nav__link">Categories</a>
			</li>
		</ul>

		<!-- tablet/ desktop Nav -->
		<ul class="mainNav" v-if="!isMobile">
      <li>
				<a href="#" class="nav__link">Home</a>
			</li>
			<li>
				<a href="#" class="nav__link">New</a>
			</li>
			<li>
				<a href="#" class="nav__link">Popular</a>
			</li>
			<li>
				<a href="#" class="nav__link">Trending</a>
			</li>
			<li>
				<a href="#" class="nav__link">Categories</a>
			</li>
		</ul>
	</nav>
</template>

<script>
export default {
	name: "AppNav",
	data() {
		return {
			isMobile: null,
      windowWidth: null,
      mobileNav: null,
		};
	},
	methods: {
    toggleMobileNav() {
      this.mobileNav = !this.mobileNav
    },
    checkScreen() {
      this.windowWidth = window.innerWidth;
      if (this.windowWidth <= 992) {
        this.isMobile = true;
        return
      }
      this.isMobile = false;
      this.mobileNav = false;
      return
    }
  },
  mounted() { },
  created() {
    window.addEventListener("resize", this.checkScreen)
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
  width: 100%;
	max-width: 60%;
	background-color: #fff;
	padding: 2em;
  display: flex;
  flex-direction: column;
}

.mobileNav li {
  margin-top: 1.5em;
}
.close {
  margin-bottom: 3em;
  display: inline-block;
  margin-left: auto;
}
.nav__link {
  color: var(--VeryDarkBlue);
  font-weight: var(--fw-bold);
}
.nav__link:hover {
  letter-spacing: 1px;
}

.mainNav {
  display: flex;
  gap: 2em;
}

@media (min-width: 470px) {
  .mobileNav {
	max-width: 18.5em;
}
}
</style>
