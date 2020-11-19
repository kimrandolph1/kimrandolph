<script lang="ts">
	import Header from '../components/Header.svelte';
	import Footer from '../components/Footer.svelte';
	
</script>

<style>
	main {
		position: relative;
		/* max-width: 56em; */
		background-color: white;
		padding: 2em;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>

<!-- <Nav {segment}/> -->
<Header />
<main>
	<slot></slot>
</main>
<Footer />