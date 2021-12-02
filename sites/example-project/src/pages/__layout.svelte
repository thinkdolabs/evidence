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
		<h1>Campus Energy</h1>
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
	  <div class=content>
		<article>
			<slot/>
		</article>
		<aside class='toc'>
		  <div class="sticky-toc">
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
	  </div>
	</main>

  </div>

<style>
.grid {
  --header-height: 2em;
  display: grid;
  grid-template-areas:
    'sidebar header'
    'sidebar main';
  grid-template-columns: 20rem 5fr;
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
  background-color: rgba(255, 255, 255, 1);

}

/*
  The “aside” child is positioned according to
  grid layout, filling the assigned grid area.
*/
aside.sidebar {
  grid-area: sidebar;
  position: relative;
  z-index: 1;
  background-color: var(--grey-100);
  border-right: 1px solid var(--grey-300);
  
  /* color: white; */
  /* border: 3px solid; */

}

.sticky {
	position: sticky;
  	top: 0;
	padding: 1em;
}

nav {
	max-height: 75vh;
	overflow-y: scroll;
}

main {
  grid-area: main;
  /* border: 3px solid; */
}

div.content { 
	margin: auto;
	max-width:100ch;
	box-sizing: border-box;
	display: grid;
	/* border: 3px solid red; */
	grid-template-columns: 4fr minmax(0,1fr);
	gap: 0 5ch;
  	grid-template-areas:
    	'article toc'; 
    justify-items: left;
}

article {
	max-width: 70ch;
	grid-area: article;
	padding: 0 1.5em 0 1.5em;
	box-sizing: border-box;
	/* border: 3px solid yellow; */
}

aside.toc {
	grid-area: toc;
	padding: 0px;
	/* border: 3px solid; */
}

.sticky-toc > h4 {
	margin-top: 0px;
}

.sticky-toc { 
	position: sticky;
  	top: var(--header-height);
	padding-left: 1em; 
	border-left: 1px solid var(--grey-100);
}


</style>