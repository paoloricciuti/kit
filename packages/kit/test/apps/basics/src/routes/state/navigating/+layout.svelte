<script>
	import { navigating } from '$app/state';
</script>

<nav>
	<a href="/state/navigating/a">a</a>
	<a href="/state/navigating/b">b</a>
	<a href="/state/navigating/c">c</a>
</nav>

<div id="nav-status">
	{#if navigating.current}
		<!-- prettier-ignore -->
		<p id="navigating">
			navigating from {navigating.current.from.url.pathname} to {navigating.current.to.url.pathname} ({navigating.current.type})
		</p>
	{:else}
		<p id="not-navigating">not currently navigating</p>
	{/if}
</div>

<slot />
