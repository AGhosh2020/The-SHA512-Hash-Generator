<script>
	import Header from'./components/header.svelte';
	import DarkMode from './components/darkmode.svelte';
	import Info from'./components/info.svelte';
	import Work from'./components/work.svelte';
	import Footer from './components/footer.svelte';
</script>
<svelte:head> 	
  <title>SHA512 Hash Generator</title>
</svelte:head>
<main>
	<Header/>
	<hr>
	<Info/>
	<div style="text-align:center;">
		<DarkMode/>  
	</div>     
	<Work/>
	<Footer/>
</main>

<style>
	@font-face{
		font-family: "Space Grotesk";
		src:url('/font/SpaceGrotesk[wght].ttf')
	}
	:global(body){
		font-family: "Space Grotesk";
		transition: background-color 0.9s;
	}
	hr{
		border:0.5px solid grey;
	}
	:global(body.dark) {
		background-color: black;
		color: #FFFFFF;
	}
</style>