<script setup lang="ts"></script>

<template>
	<section>
		<div class="menu">
			<div class="marquee">
				<div class="marquee__inner">
					<span>Showreel</span>
					<span>Showreel</span>
					<span>Showreel</span>
					<span>Showreel</span>
				</div>
			</div>
		</div>
	</section>
</template>
  
<style scoped>
section {
	margin: 0;
	--color-text: #dedede;
	--color-bg: #1a1a1a;
	color: var(--color-text);
	background-color: var(--color-bg);
}

.menu {
	padding: 10vh 0 25vh;
	--marquee-width: 100vw;
	--offset: 20vw;
	--move-initial: calc(-25% + var(--offset));
	--move-final: calc(-50% + var(--offset));
	--item-font-size: 10vw;
	counter-reset: menu;
	-webkit-touch-callout: none;
	-webkit-user-select: none;
	-moz-user-select: none;
	-ms-user-select: none;
	user-select: none;
}

/* Make sure 3 items are visible in the viewport by setting suitable font size. */

.marquee {
	position: absolute;
	top: 0;
	left: 0;
	width: var(--marquee-width);
	overflow: hidden;
}

.marquee__inner {
	width: fit-content;
	display: flex;
	position: relative;
	transform: translate3d(var(--move-initial), 0, 0);
	animation: marquee 5s linear infinite;
	animation-play-state: paused;
	opacity: 0;
	transition: opacity 0.1s;
}

.marquee .marquee__inner {
	animation-play-state: running;
	opacity: 1;
	transition-duration: 0.4s;
}

/* .marquee .marquee__inner:hover {
	animation-play-state: paused;
} */

.marquee span {
  text-align: center;
	white-space: nowrap;
	font-size: var(--item-font-size);
	padding: 0 1vw;
	font-weight: 900;
	line-height: 1.15;
  font-style: italic;
}

@keyframes marquee {
	0% {
		transform: translate3d(var(--move-initial), 0, 0);
	}

	100% {
		transform: translate3d(var(--move-final), 0, 0);
	}
}
</style>
  