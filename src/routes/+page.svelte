<script>
	import LayoutLfeft from "../components/layoutLeft.svelte";
	import LayoutRight from "../components/layoutRight.svelte";
</script>
<svelte:head>
	<title>Layout</title>
	<meta name="description" content="Layout page title" />
</svelte:head>
<div class="layout">
	<h1 class="mb-4 text-3xl text-[#980000]">Layout Page:</h1>
	<div class="md:flex">
		<div class="w-full h-full md:w-6/12">
			<LayoutLfeft/>
		</div>
		<div class="w-full h-full md:w-6/12">
			<LayoutRight />
		</div>
	</div>
</div>