<script>
	import "../app.css"
	import { navigating } from '$app/stores';
	import LoadingIndicator from '@evidence-dev/components/ui/LoadingIndicator.svelte';
	import { blur, fade } from "svelte/transition"
	import Logo from "@evidence-dev/components/ui/Logo.svelte";
	import BreadCrumbs from "@evidence-dev/components/ui/BreadCrumbs.svelte";
</script>

<svelte:head>
	<title>Evidence</title>
</svelte:head>

<div class="grid">
	<header>
	  <BreadCrumbs/>
	</header>
	<aside class=sidebar>
	  <div class="sticky">
		<h3><a href = '/' >Organization Name</a></h3>
		<nav>
		  <ul>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
			<li>Nav Item</li>
		  </ul>
		</nav>
		<div class=side-bar-bottom>
			<h1>Bottom stuff</h1>
		</div>
	  </div>
	</aside>
	<main>
	{#if !$navigating}
	  <article transition:fade>
		  <slot/>
	  </article>
	  <aside class='toc'>
		<div class="sticky">
			<h4>On this page</h4>
			  <ul>
				<li>Nav Item that is much longer than 14 rem</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
				<li>Nav Item</li>
			  </ul>
		</aside>
	{/if}
	</main>

  </div>

<style>
.grid {
  --header-height: 2em;
  display: grid;
  grid-template-areas:
    'sidebar header'
    'sidebar main';
  grid-template-columns: 14rem 1fr;
  grid-template-rows: var(--header-height) 1fr;
  gap: 0 16px;
  margin: 0 auto;
  isolation: isolate;
}

header {
  grid-area: header;
  position: sticky;
  z-index: 2;
  top: 0;
  display: grid;
  place-content: center;
  height: var(--header-height);
  /* border-bottom: 3px solid; */
  background-color: rgba(255, 255, 255, 0.95);

}

/*
  The “aside” child is positioned according to
  grid layout, filling the assigned grid area.
*/
aside.sidebar {
  grid-area: sidebar;
  position: relative;
  z-index: 1;
  padding-top: 0;
  border: 3px solid;

}

.sticky {
	position: sticky;
  	top: var(--header-height);
	margin-top: 0;
	padding-top: 0;
}

nav {
	max-height: 75vh;
	overflow-y: scroll;
}

main {
  grid-area: main;
  border: 3px solid;
  display: grid;
  gap: 0 16px;
  justify-items: center;
  grid-template-columns: 1fr 14rem;
  grid-template-areas:
    'article toc'
}

article {
	max-width: 70ch;
	grid-area: article;
}

aside.toc {
	grid-area: toc;
	border: 3px solid;
}

</style>