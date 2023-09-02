<script>
	import { page } from '$app/stores';
</script>

<header>
	<div class="container mx-auto">
		<nav>
			<ul class="flex justify-center items-center space-x-7 py-5">
				<li aria-current={$page.url.pathname==='/' ? 'page' : undefined}>
					<a href="/">Layout</a>
				</li>
				<li aria-current={$page.url.pathname==='/chart' ? 'page' : undefined}>
					<a href="/chart">Chart</a>
				</li>
				<li aria-current={$page.url.pathname==='/map' ? 'page' : undefined}>
					<a href="/map">Map</a>
				</li>
			</ul>
		</nav>
	</div>
</header>