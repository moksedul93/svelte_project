<script>
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<ul>
			<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
				<a href="/">Layout</a>
			</li>
			<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
				<a href="/about">Chart</a>
			</li>
			<li aria-current={$page.url.pathname === '/sverdle' ? 'page' : undefined}>
				<a href="/sverdle">Map</a>
			</li>
		</ul>
	</nav>
</header>
